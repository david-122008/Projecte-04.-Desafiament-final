# T09: Servidor de Fitxers Linux – NFS (Tasca Individual)

## Breu descripció
Aquesta tasca té com a objectiu implementar un **servidor de fitxers centralitzat** en entorns Linux utilitzant **NFS (Network File System)**. Es tracta d’una demostració pràctica per al client **DevOptimize Solutions**, una startup de desenvolupament de programari que necessita centralitzar el seu codi font i actius per evitar errors de versió i millorar l’eficiència.

---

## Introducció
- **Problema del client:** Cada desenvolupador té còpies locals del codi i documents, provocant descontrol i pèrdua d’eficiència.  
- **Solució proposada:** Implementar un servidor de fitxers centralitzat amb **NFSv3**, la solució nativa i eficient en entorns Linux.  
- **Condició del client:** No disposa d’un entorn d’autenticació centralitzada i, de moment, no té previst implantar-lo.  

---

## Missió
- Crear un **servidor NFS (NFSv3)**.  
- Configurar un **client Linux** que consumeixi els recursos compartits.  
- Crear **usuaris i grups** per simular l’entorn del client.  
- Demostrar el **control d’accés** mitjançant:  
  - Opcions d’exportació (`/etc/exports`).  
  - Permisos del sistema de fitxers (`chmod`, `chown`).  

---

## Repositori de la tasca
- [Projecte04-NFS (GitHub)](https://github.com/SMX2n/Projecte04-NFS)

---

## Materials i links de suport
- **Material propi:** UD5. AA1. NFS – Disponible al Moodle del mòdul de Sistemes Operatius en Xarxa.  
- Ruiz, P. (2021, novembre 22). *NFS (parte 1): Instalación en un servidor Ubuntu 20.04 LTS*. SomeBooks.es.  
  [Enllaç](https://somebooks.es/nfs-parte-1-instalacion-en-un-servidor-ubuntu-20-04-lts/)  
- Ruiz, P. (2021, desembre 2). *NFS (parte 2): Instalación en un cliente Ubuntu 20.04 LTS*. SomeBooks.es.  
  [Enllaç](https://somebooks.es/nfs-parte-2-instalacion-en-un-cliente-ubuntu-20-04-lts/)  
- *Network File System (NFS)*. Ubuntu Server Documentation.  
  [Enllaç](https://documentation.ubuntu.com/server/how-to/networking/install-nfs/)  
