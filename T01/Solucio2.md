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

