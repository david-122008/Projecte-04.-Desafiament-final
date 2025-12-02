# T01: DRP – Còpies de Seguretat  
**Estudi de cas client: Muntatges i Serveis Tècnics SL**  
Treball cooperatiu

---

## Breu descripció
Aquest projecte té com a objectiu dissenyar una política de còpies de seguretat per a una petita empresa dedicada a la instal·lació i manteniment d’equips industrials. El treball es divideix en tres fases: individual, per parelles i en grup, amb la finalitat d’arribar a una proposta consensuada i professional.

---

## Introducció
Durant la primera hora, el responsable de seguretat presenta el tema de les còpies de seguretat amb material didàctic. Posteriorment, els alumnes treballen els aspectes clau mitjançant dinàmiques cooperatives, aplicant-los a un cas pràctic realista.

---

## Presentació del cas client
**Empresa:** Muntatges i Serveis Tècnics SL  
**Infraestructura tècnica:**
- **Servidor de fitxers (Ubuntu Server):**
  - Documents de projectes (300 GB, creixement moderat).  
  - Bases de dades de comptabilitat i clients (20 GB, ús diari, canvi constant).  
  - Carpetes personals dels usuaris (100 GB).  
- **10 equips clients (Windows 10/11):** ús principal del servidor, amb alguns arxius temporals locals.  
- **Connexió a Internet:** fibra òptica simètrica de 600 Mbps.  

**Requisits de recuperació:**
- **RTO (Recovery Time Objective):** dades de Comptabilitat/Clients disponibles en menys de 4 hores.  
- **RPO (Recovery Point Objective):** pèrdua màxima de 24 h per a la majoria de dades; màxim 4 h per a Comptabilitat/Clients.  
- **Retenció:** historial mínim d’un mes.  

---

## Fase 1: Treball individual
1. **Què copiar (priorització):**  
   - Dades més crítiques: Bases de dades de Comptabilitat/Clients.  
   - Documents de projectes i carpetes personals també s’han de copiar, però amb menor prioritat.  
   - Els equips clients no són crítics: només cal fer còpia de carpetes Documents si contenen informació rellevant.  

2. **Periodicitat i tipus de còpia:**  
   - **Bases de dades (crítiques):** còpia incremental cada 4 h + còpia completa diària.  
   - **Documents de projectes:** còpia diferencial diària + còpia completa setmanal.  
   - **Carpetes personals:** còpia completa setmanal.  

3. **Mitjans i ubicació (Regla 3-2-1):**  
   - **Mitjà local:** NAS intern amb discs redundants.  
   - **Mitjà extern:** Cloud (Azure/Google Cloud) amb retenció d’un mes.  
   - **Ubicació fora de lloc:** còpia externa al núvol gestionada pel responsable de seguretat.  

---

## Fase 2: Treball per parelles
**Esquema 3-2-1 consensuat:**

| Element              | Proposta de la parella                          | Justificació                                                                 |
|----------------------|-------------------------------------------------|-------------------------------------------------------------------------------|
| Dades crítiques      | Bases de dades Comptabilitat/Clients            | Ús constant i requisit de RTO/RPO estricte.                                   |
| Periodicitat (BD)    | Incremental cada 4 h + completa diària          | Garantir pèrdua màxima de 4 h i recuperació ràpida.                           |
| Tipus de còpia (BD)  | Incremental + completa                          | Optimitza espai i temps de còpia.                                            |
| Mitjà 1 (Local)      | NAS amb RAID                                    | Alta disponibilitat i recuperació ràpida.                                    |
| Mitjà 2 (Extern)     | Cloud (Azure/Google Cloud)                      | Ubicació fora de lloc, escalabilitat i seguretat.                            |

---

## Fase 3: Treball en grup
**Política de còpies de seguretat definitiva:**

1. **Dades objecte de còpia:**
   - **Servidor:**  
     - BD Comptabilitat/Clients → còpia incremental cada 4 h + completa diària.  
     - Documents de projectes → diferencial diària + completa setmanal.  
     - Carpetes personals → completa setmanal.  
   - **Equips clients:** còpia mensual de carpetes Documents si contenen informació rellevant.  

2. **Cronograma setmanal detallat:**

| Dia      | Dades                   | Tipus de còpia        | Mitjà         |
|----------|-------------------------|-----------------------|---------------|
| Dilluns  | BD Comptabilitat/Clients| Incremental + completa| NAS + Cloud   |
| Dimarts  | Documents de projectes  | Diferencial           | NAS           |
| Dimecres | BD Comptabilitat/Clients| Incremental           | NAS           |
| Dijous   | Carpetes personals      | Completa              | NAS           |
| Divendres| BD Comptabilitat/Clients| Incremental + completa| NAS + Cloud   |
| Dissabte | Documents de projectes  | Completa              | Cloud         |
| Diumenge | BD Comptabilitat/Clients| Incremental           | NAS           |

3. **Elecció de mitjans i ubicació (Regla 3-2-1):**
   - **Mitjà 1 (Local):** NAS amb discs redundants (RAID).  
   - **Mitjà 2 (Extern):** Cloud (Azure/Google Cloud).  
   - **Ubicació fora de lloc:** còpia externa al núvol, gestionada pel responsable de seguretat.  

4. **Estratègia de recuperació (RTO/RPO):**
   - Les BD Comptabilitat/Clients es copien cada 4 h (RPO ≤ 4 h).  
   - Les còpies incrementals i completes permeten restaurar en menys de 4 h (RTO ≤ 4 h).  
   - Les dades menys crítiques tenen RPO de 24 h i RTO flexible.  

---

## Materials i links de suport
- Moodle 0226 Seguretat Informàtica. RA2.AA3Còpies  
- INCIBE. *Copias de seguridad. Una guía de aproximación para el empresario*  
- Xataka. *Backup 3-2-1, el método definitivo para mantener a salvo tus datos* [YouTube, 2017]  
  https://youtu.be/PM_M4Iz6I4o?si=F7DRyDDTZE3hjWn8

a l'arxiu [solució.md](Solucio1.md) hia la part individual
