# T07: Accés Remot – Serveis d’Assistència Remota (Tasca en Parelles)

## Breu descripció
Fins ara hem vist eines per administrar servidors (SSH, RDP, VNC). Però la realitat de la nostra feina a EverPia és que una gran part de les hores facturables provenen del **suport directe a l’usuari final (Helpdesk)**.  

Quan un client truca perquè *“el PDF no s’obre”*, *“li ha desaparegut una icona”* o *“la impressora no imprimeix”*, no li podem demanar que configuri una VPN o obri el port 3389 del seu router. Necessitem una eina d’assistència remota sota demanda: **ràpida, fiable, segura i que funcioni en segons, fins i tot en xarxes restrictives**.

La direcció d’EverPia ha decidit estandarditzar l’eina oficial per a aquestes tasques de suport immediat. La missió en parelles és **analitzar el mercat i proposar la millor solució**, per després crear la documentació que faran servir tant els tècnics com els clients.

---

## Fase 1: Anàlisi Comparativa i Selecció de la Solució

### Tasques
- Investigar quatre alternatives populars d’assistència remota.  
  - Exemples obligatoris: **TeamViewer, AnyDesk, Google Remote Desktop**.  
  - Afegir una quarta eina de lliure elecció.  
- Crear una **taula comparativa** que avaluï cada solució segons criteris clau:
  - **Facilitat d’ús (per al client):** Requereix instal·lació? És portable? És senzill per a un usuari no tècnic?  
  - **Disponibilitat (Sistemes Operatius):** Funciona a Windows, macOS, Linux?  
  - **Model de Preu (Llicència):** És gratuït per a ús comercial? Cost de llicència per tècnic? Limitacions de la versió gratuïta?  
- Presentar una **recomanació oficial**: escollir una eina i justificar per què és la millor opció (equilibri entre facilitat, funcionalitat i cost).

---

## Fase 2: Creació de les Guies d’Ús (Documentació)

### Guia 1: Manual per al Tècnic (Intern d’EverPia)
- Destinat a futurs becaris i tècnics.  
- Ha d’explicar el flux de treball des del punt de vista del consultor.  
- Incloure (amb captures de pantalla):  
  - Instal·lació de la versió completa/tècnica de l’eina.  
  - Inici d’una sessió de suport.  
  - Gestió de funcions clau (transferència d’arxius, canvi de pantalla, reinici remot).  
  - Bones pràctiques de seguretat (tancar sempre la sessió, no desar contrasenyes de clients).  

### Guia 2: Manual per al Client (Usuari Final)
- Guia que s’enviarà als clients quan tinguin una incidència.  
- Ha de ser **extremadament simple, visual i no tècnica**.  
- Incloure (amb captures de pantalla clares):  
  - Enllaç o mètode per descarregar el mòdul *Quick Support* (o equivalent, sense instal·lació).  
  - On han de fer clic exactament.  
  - Com identificar i comunicar al tècnic l’ID de sessió i la contrasenya (si n’hi ha).  
  - Com acceptar la petició de connexió.  

---

## Materials i links de suport
- [Genbeta – Software per donar suport remot](https://www.genbeta.com/a-fondo/que-software-instalar-a-tus-familiares-amigos-para-darles-soporte-ayuda-remoto)  
- [Genbeta – RustDesk com a alternativa a TeamViewer](https://www.genbeta.com/herramientas/necesitas-escritorio-remoto-puedes-decirle-adios-a-teamviewer-rustdesk-gratis-e-ideal-para-usar-pc-movil)  
- [Genbeta – Chrome Remote Desktop](https://www.genbeta.com/herramientas/chrome-remote-desktop-que-como-funciona-como-puedes-usarlo-para-controlar-tu-pc-forma-remota)  
