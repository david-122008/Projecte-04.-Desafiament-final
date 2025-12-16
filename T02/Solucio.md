# **T02: DPR: còpies de seguretat. Cas pràctic**

![Imatge 01](IMG/ING1.png)
![Imatge 01](IMG/ING2.png)

Primer crearem una màquina virtual a la qual li afegirem un disc de 10 GB que servirà per emmagatzemar les copiés de seguretat.

![Imatge 01](IMG/ING3.png)
![Imatge 01](IMG/ING4.png)
![Imatge 01](IMG/ING5.png)

Després anirem a administrar espais d'emmagatzematge, crearem un grup d’emmagatzematge, creem el grup i creem l’espai d'emmagatzematge.

![Imatge 01](IMG/ING6.png)

Instal·lem duplicati.

![Imatge 01](IMG/ING7.png)

I creem les còpies de seguretat

![Imatge 01](IMG/ING8.png)

Posem nom a la còpia de seguretat, la descripció i la contrasenya.

![Imatge 01](IMG/ING9.png)

Després clicarem l’opció de file system

![Imatge 01](IMG/ING10.png)

Escollirem el disc secundari,

![Imatge 01](IMG/ING11.png)

Després escollim la carpeta que volem copiar, en el nostre cas Home, on tenim documents,
downloads etc.

![Imatge 01](IMG/ING12.png)
![Imatge 01](IMG/ING13.png)

En aquest apartat s’estableix que les còpies de seguretat es facin cada hora i es desin al disc secundari, a l’apartat Options es deixa activada l’opció Keep all backups perquè no s’esborri cap còpia, finalment, es prem Submit, però abans cal registrar-se perquè el sistema ho permeti.

![Imatge 01](IMG/ING14.png)

Un cop creat, afegirem arxius a les carpetes de l’usuari, especialment documents, després farà les còpies corresponents en els moments corresponents al lloc el funcionament.

![Imatge 01](IMG/ING15.png)

Ara creem l'altra còpia de seguretat, pel Drive, després posem un altre cop nom a la còpia de seguretat una descripció i una contrasenya.

![Imatge 01](IMG/ING16.png)

Però ara cliquem l’opció de Drive en comptes de file system.

![Imatge 01](IMG/ING17.png)

Tornem a escollir una carpeta.

![Imatge 01](IMG/ING18.png)
![Imatge 01](IMG/ING19.png)

Aquí indicarem que les còpies de seguretat es faran cada dia a les 18:00 i es desaran al Drive. A l’apartat Options mantindrem activada l’opció Keep all backups perquè no s’esborri cap còpia. Finalment, només cal prémer Submit per confirmar la configuració.

![Imatge 01](IMG/ING20.png)
![Imatge 01](IMG/ING21.png)

Cal generar un AuthID perquè la còpia de seguretat al Drive funcioni quan es prem Start i apareix un error, s’obre l’enllaç que mostra la notificació, es copia el text que apareix al navegador i s’enganxa a l’apartat AuthID dins de Destination a la configuració del backup. Un cop fet això, la còpia ja funcionarà correctament.

![Imatge 01](IMG/ING22.png)
![Imatge 01](IMG/ING23.png)

Un cop creat, afegirem arxius a les carpetes de l’usuari, especialment a documents, després farà les còpies corresponents en corresponents al lloc el funcionament.
Després els esborrem, per fer la comprovació

![Imatge 01](IMG/ING24.png)

Després farem la Restauració des del disc secundari, anirem a restore i escollim l'opció de còpia de seguretat disc secundari i cliquem en restore.

![Imatge 01](IMG/ING25.png)

Hem de seleccionar els fitxers, i confirmem correctament, i li donarem a continue.

![Imatge 01](IMG/ING26.png)

Original location i Overwrite. I Ssubmit

![Imatge 01](IMG/ING27.png)

I la restauració estaria completada i en teoria ja se'ns haurien recuperat els arxius

![Imatge 01](IMG/ING28.png)

I les còpies de seguretat que crea duplicati apareixeran tant al disc secundari com al Google Drive en forma d’arxius encriptats, si entrem al Google Drive, podem veure aquests fitxers generats pel programa

![Imatge 01](IMG/ING29.png)

