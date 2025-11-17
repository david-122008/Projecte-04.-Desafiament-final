# T02: DPR – Còpies de Seguretat. Cas Pràctic

## Breu descripció
Introducció al cas  
A la tasca anterior heu dissenyat una política de còpies de seguretat pel nostre nou client **"Muntatges i Serveis Tècnics SL"**. Ara toca passar a l’acció i portar a la pràctica l’estudi anterior. El client demana que s’elaborin unes guies tècniques amb proves de concepte per tal que el seu personal estigui qualificat per implantar el pla de còpies de seguretat.

---

## Part 1: Còpia seguretat dels equips clients Windows
Encara que en principi el DPR no contemplaria fer còpia dels arxius locals dels equips clients, se’ns demana fer una excepció amb l’equip Windows del director de l’empresa. En aquest equip es guarda informació important que no es vol tenir accessible al servidor de fitxers de l’empresa. Per aquest motiu és necessari definir una política de còpies de seguretat seguint l’esquema **3-2-1**:  
- Es farà una còpia de seguretat a un disc secundari que té el propi equip.  
- Una segona còpia al **cloud**, en aquest cas, Google Drive usant l’eina **Duplicati**.

### Prova de concepte
- Crear una màquina virtual Windows 11 amb dos discos:  
  - Un per al sistema operatiu.  
  - Un secundari de 10 GB per emmagatzemar les còpies de seguretat.  
- Per simular la part de Google Drive, usar un compte que no sigui el d’escola (crear-ne un específic per l’activitat).  
- Es desitja fer còpies de seguretat del perfil de l’usuari:  
  - Cada hora al disc secundari.  
  - A les 18:00 a Google Drive.  

### Tasques
- Documentar el procediment d’instal·lació de Duplicati.  
- Configurar els plans de còpies i observar el funcionament.  
- Afegir arxius a les carpetes de l’usuari (especialment a Documents).  
- Esborrar el contingut de Documents i restaurar des del disc secundari.  
- Comprovar la restauració des de la còpia emmagatzemada al cloud.  

---

## Part 2: Còpia seguretat servidor Linux
Per fer les còpies del servidor Linux la solució proposada és **Duplicity**, que permet fer còpies tant contra un mitjà local com contra un servidor remot. Combinat amb el programador de tasques (**cron**) es poden implementar les polítiques de còpia desitjades.

### Prova de concepte
- Crear una màquina virtual amb **Ubuntu Server**.  
- Afegir un segon disc de 10 GB que simularà una unitat auxiliar.  

### Passos
1. Inicialitzar i formatar en format **xfs**. Muntar manualment a `/media/backup` (crear la carpeta).  
2. Instal·lar **duplicity**.  
3. Crear un parell d’usuaris més al sistema amb carpeta personal. Crear 4 arxius de 10 MB a la carpeta home de l’usuari.  
4. Fer una còpia de seguretat de la carpeta `/home`.  
5. Esborrar els arxius i fer un restore per comprovar la recuperació.  
6. Afegir un nou arxiu de 4 MB i fer una nova còpia. Observar com ara es fa una còpia incremental.  
7. Desmuntar la unitat de backup.  

### Automatització amb scripts
- **fullbackup.sh**  
  - Realitza la còpia completa de la carpeta `/home` i l’emmagatzema al volum muntat.  
  - Usa la variable d’entorn `PASSPHRASE`.  
  - Donar permisos d’execució.  
  - Programar al cron com a root els diumenges a les 23:00.  

- **incrementalbackup.sh**  
  - Realitza còpies incrementals de la mateixa carpeta.  
  - Fixar el valor de la variable `PASSPHRASE`.  
  - Donar permisos d’execució.  
  - Programar al cron com a root de dilluns a dissabte a les 
