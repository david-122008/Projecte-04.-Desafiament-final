# Fase 2: Treball per Parelles

## Elaboració d'una Proposta Unificada  
Heu de consensuar i dissenyar el vostre propi **Esquema 3-2-1 de Còpies**  
(3 còpies, 2 mitjans, 1 fora de lloc) basat en els requisits del cas.

---

## 📌 Proposta d’Esquema 3-2-1

| **Element** | **Proposta de la Parella** | **Justificació** |
|-------------|-----------------------------|-------------------|
| **Dades Crítiques** | - Bases de Dades (Comptabilitat i Clients)  <br> - Documents de Projectes  <br> - Carpetes Personals  <br> - Carpeta Documents dels equips Windows | Les BD tenen canvis constants i necessiten RTO/RPO molt baixos. Documents de Projectes i Carpetes Personals tenen més volum però menys urgència. Els equips clients només requereixen arxius puntuals. |
| **Periodicitat (BD)** | - Incremental **cada 4 hores**  <br> - Diferencial **diària**  <br> - Completa **setmanal**  <br> - Completa **mensual** | Garanteix una pèrdua màxima de 4 h (RPO). Les còpies diàries i setmanals creen punts de restauració estables. El mensual aporta un històric segur. |
| **Tipus de Còpia (BD)** | - Incrementals per canvis constants <br> - Diferencial setmanal per restauració ràpida <br> - Completes com a base fiable | Restauració flexible: les incrementals cobreixen el dia, diferencial accelera restauració, i la completa dona una base estable. |
| **Mitjà 1 (Local)** | NAS intern per a còpies incrementals i diferencials | Restauració ràpida, centralitzada i amb alta velocitat dins la xarxa. Ideal per snapshots i automatització. |
| **Mitjà 2 (Extern)** | - Disc dur extern (còpia setmanal) <br> - Cloud (còpia mensual) | Compleix la regla 3-2-1. Mitjà diferent + còpia off-site per protegir-se de robatoris, incendis o desastres. |

---

## ✔ Resum del nostre esquema 3-2-1

- **3 còpies:** Local al NAS + Disc extern + Núvol  
- **2 mitjans diferents:** NAS / disc extern / cloud  
- **1 còpia fora de lloc:** Núvol (off-site)

---

# Fase 3: Treball per grup

## 2. Elaboració d'una Proposta Unificada
Heu de consensuar i dissenyar el vostre propi **Esquema 3-2-1 de Còpies** (3 còpies, 2 mitjans, 1 fora de lloc) basat en els requisits del cas.

### Taula de Proposta
| Element              | Proposta de la Parella                                                                 | Justificació                                                                                                         |
|----------------------|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| **Dades Crítiques**  | - Bases de Dades (Comptabilitat i Clients)<br>- Documents de Projectes<br>- Carpetes Personals<br>- Carpeta Documents dels clients Windows | Les BD tenen dades de canvi constant i necessiten RTO/RPO molt baixos. Documents de Projectes i Carpetes Personals tenen gran volum però menys criticitat temporal. Els equips només necessiten arxius puntuals. |
| **Periodicitat (BD)**| - Incremental cada 4 hores<br>- Diferencial diària<br>- Completa setmanal<br>- Completa mensual | Garanteix la pèrdua màxima de 4 h (RPO). Les còpies diàries i setmanals generen punts de restauració estables i historial mensual. |
| **Tipus de Còpia (BD)**| - Incrementals per capturar canvis constants<br>- Diferencial setmanal per restauració ràpida<br>- Completes com a base fiable | Restauració flexible: les incrementals cobreixen el dia, la diferencial facilita restauració i la completa ofereix punt segur. |
| **Mitjà 1 (Local)**  | - NAS intern per a còpies incrementals i diferencials                                   | Restauració ràpida i centralitzada. Alta velocitat en xarxa interna i snapshots.                                     |
| **Mitjà 2 (Extern)** | - Disc dur extern per còpia setmanal<br>- Núvol per còpia mensual                        | Compleix la regla 3-2-1: mitjà diferent i còpia off-site protegida davant robatori, incendi o desastre físic.        |

---

# Fase 3: Treball en grup

## 1. Debat i Selecció
Cada parella presenta el seu esquema. El grup debat els pros i contres de cada proposta (cost, temps de recuperació, seguretat, simplicitat).

## 2. Disseny de la Política Final
El grup ha de redactar la **Política de Còpies de Seguretat Definitiva** que presentaran a l'empresa *Muntatges i Serveis Tècnics SL*.

### 1) Dades Objecte de Còpia
| Tipus                        | Objecte de Còpia                          | Criticitat | Comentari                                      |
|------------------------------|--------------------------------------------|------------|------------------------------------------------|
| Servidor de Fitxers (Ubuntu) | Bases de Dades (Comptabilitat i Clients)   | Alta       | Canvi constant, RPO 4h, RTO 4h                 |
|                              | Documents de Projectes                     | Mitjana    | Gran volum, canvis moderats                    |
|                              | Carpetes Personals dels Usuaris            | Mitjana    | Canvis diaris                                  |
| Equips Clients (Windows 10/11)| Carpeta Documents                         | Mitjana    | Alguns informes i arxius temporals             |

### 2) Cronograma Setmanal Detallat
| Dia       | Dades              | Tipus de Còpia                          | Mitjà                 |
|-----------|--------------------|-----------------------------------------|-----------------------|
| Dilluns   | Bases de Dades     | Incremental cada 4h                     | NAS                   |
|           | Documents Projectes| Incremental diari                       | NAS                   |
|           | Carpetes Personals | Incremental diari                       | NAS                   |
|           | Clients Windows    | Incremental diari                       | NAS                   |
| Dimarts   | Bases de Dades     | Incremental cada 4h                     | NAS                   |
|           | Documents Projectes| Incremental diari                       | NAS                   |
|           | Carpetes Personals | Incremental diari                       | NAS                   |
|           | Clients Windows    | Incremental diari                       | NAS                   |
| Dimecres  | Bases de Dades     | Incremental cada 4h                     | NAS                   |
|           | Documents Projectes| Incremental diari                       | NAS                   |
|           | Carpetes Personals | Incremental diari                       | NAS                   |
|           | Clients Windows    | Incremental diari                       | NAS                   |
| Dijous    | Bases de Dades     | Incremental cada 4h                     | NAS                   |
|           | Documents Projectes| Incremental diari                       | NAS                   |
|           | Carpetes Personals | Incremental diari                       | NAS                   |
|           | Clients Windows    | Incremental diari                       | NAS                   |
| Divendres | Bases de Dades     | Diferencial diària + Completa setmanal  | NAS + Disc dur extern |
|           | Documents Projectes| Completa setmanal                       | Disc dur extern       |
|           | Carpetes Personals | Completa setmanal                       | Disc dur extern       |
|           | Clients Windows    | Incremental diari                       | NAS                   |
| Dissabte  | Bases de Dades     | Incremental cada 4h                     | NAS                   |
|           | Documents Projectes| Incremental diari                       | NAS                   |
|           | Carpetes Personals | Incremental diari                       | NAS                   |
|           | Clients Windows    | Incremental diari                       | NAS                   |
| Diumenge  | Bases de Dades     | Completa mensual                        | Cloud (AWS)           |
|           | Documents Projectes| Completa mensual                        | Cloud (AWS)           |
|           | Carpetes Personals | Completa mensual                        | Cloud (AWS)           |

### 3) Elecció de Mitjans i Ubicació (Regla 3-2-1)
| Categoria             | Mitjà                  | Ubicació                        | Responsabilitat                  |
|-----------------------|------------------------|---------------------------------|----------------------------------|
| Mitjà 1 (Local)       | NAS intern             | Sala de Servidors, accés restringit | Administrador TI              |
| Mitjà 2 (Extern)      | Disc dur extern (setmanal) | Armaris segurs a l’empresa     | Administrador TI                 |
| Ubicació Fora de Lloc | Cloud (AWS)            | Servei Cloud, dades xifrades    | Administrador TI i responsable seguretat |

> Aquest esquema compleix la regla **3-2-1**: tenim 3 còpies (NAS, disc extern, cloud), 2 mitjans diferents (NAS + disc extern/cloud), i 1 fora de lloc (Cloud).

### 4) Estratègia de Recuperació (RTO/RPO)
**Bases de Dades (Comptabilitat/Clients):**
- **RPO 4 h:** Còpies incrementals cada 4 hores per minimitzar pèrdua de dades.  
- **RTO 4 h:** Restauració prioritària des del NAS o, si cal, des del disc dur extern. El cloud actua com a última via en cas de desastre major.  

**Documents de Projectes / Carpetes Personals / Clients Windows:**
- **RPO 24 h:** Còpies incrementals diàries asseguren que només es perd un dia de treball.  
- **RTO ≤ 24 h:** Restauració ràpida des del NAS per incidents menors.  

**Procediment en cas de fallada:**
1. Restaurar dades crítiques (BD) des del NAS.  
2. Si el NAS no està disponible, utilitzar disc extern.  
3. En cas de desastre total, recuperar còpia mensual des del Cloud.  


[torna al enunciat](README.md)
