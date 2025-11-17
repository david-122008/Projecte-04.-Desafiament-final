# T03: Pla de Recuperació davant Desastres – Imatges del Sistema

## Breu descripció
Aquest projecte forma part del **Pla de Contingència i Continuïtat del Negoci** del client *Muntatges i Serveis Tècnics SL*. L’objectiu és posar en marxa un **Pla de Recuperació davant Desastres (DRP)** que permeti restaurar dades, hardware i software crític de manera ràpida i eficient.  
Un dels punts clau és assegurar que els treballadors disposin d’imatges de restauració dels seus equips (Zorin OS 18), per reduir el temps de posada en marxa en cas de robatori, avaria o incidència greu.

---

## Introducció al cas
- El client utilitza **Zorin OS 18** amb aplicacions ja configurades.  
- El temps de recuperació és crític: no és viable reinstal·lar manualment sistema, configuracions i aplicacions.  
- Es requereix una solució que permeti crear i restaurar imatges completes del sistema.  

---

## Fase 1: Anàlisi i Justificació de la Solució Tècnica

### Comparativa d’eines

| Tipus        | Producte           | Característiques destacades                                                                 | Preu aproximat |
|--------------|-------------------|---------------------------------------------------------------------------------------------|----------------|
| Comercial    | **Acronis Cyber Protect Home Office** | - Imatges completes de disc<br>- Opcions de clonació<br>- Integració amb núvol<br>- Interfície intuïtiva | Subscripció anual (~50–80 €) |
| Comercial    | **Paragon Hard Disk Manager**         | - Gestió avançada de particions<br>- Còpies incrementals i diferencials<br>- Restauració ràpida | Llicència (~80–100 €) |
| Comunitat    | **Clonezilla**                        | - Eina lliure i gratuïta<br>- Suporta múltiples formats<br>- Molt utilitzada en entorns educatius i empresarials | Gratuït |
| Comunitat    | **Rescuezilla**                       | - Interfície gràfica senzilla<br>- Basat en Clonezilla<br>- Compatible amb múltiples formats<br>- Ideal per usuaris no experts | Gratuït |

### Proposta
Es proposa l’ús de **Rescuezilla** com a solució inicial:  
- **Raons:**  
  - Gratuït i de comunitat, sense cost de llicència.  
  - Interfície gràfica senzilla, fàcil per al personal de manteniment.  
  - Basat en Clonezilla, amb compatibilitat i fiabilitat provada.  
  - Ideal per a proves de concepte i entorns on es requereix rapidesa i simplicitat.  

---

## Fase 2: Guia d’Ús Tècnica (Manual Operatiu)

### Objectiu
- Crear una imatge completa del sistema (Zorin OS 18).  
- Restaurar la imatge sobre un sistema net (màquina virtual idèntica).  

### Procediment amb Rescuezilla

1. **Preparació:**
   - Descarregar l’ISO de Rescuezilla.  
   - Crear una màquina virtual amb les mateixes característiques que l’original (RAM, CPU, disc).  
   - Afegir un disc extern o unitat per emmagatzemar la imatge.  

2. **Creació de la imatge:**
   - Iniciar la màquina amb Rescuezilla (boot des de l’ISO).  
   - Seleccionar l’opció *Backup*.  
   - Escollir el disc origen (Zorin OS 18).  
   - Definir el destí (disc extern o carpeta compartida).  
   - Executar la còpia i verificar que la imatge s’ha creat correctament.  

3. **Restauració de la imatge:**
   - Iniciar la màquina neta amb Rescuezilla.  
   - Seleccionar l’opció *Restore*.  
   - Escollir la imatge prèviament creada.  
   - Definir el disc destí (nou disc buit).  
   - Executar la restauració.  
   - Comprovar que el sistema arrenca amb les configuracions i aplicacions originals.  

---

## Resultat esperat
- El personal de manteniment pot crear i restaurar imatges de manera senzilla.  
- Es garanteix un temps de recuperació molt inferior al d’una reinstal·lació manual.  
- La solució és escalable i pot aplicar-se a tots els equips de l’empresa.  

---
**Nota:** Aquesta tasca és individual i forma part de la prova de concepte per validar l’ús de Rescuezilla com a eina principal dins el 
