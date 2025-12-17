

![Imatge 01](IMA/ING1.png)
Primer creem el segon disc de 10 GB

![Imatge 01](IMA/ING2.png)

Entrem a la màquina Linux i comprovem que detecta el segon disc amb la següent comanda

![Imatge 01](IMA/ING3.png)

Ara crearem una partició nova en el segon disc de 10GB, posarem primer N nova partició, P partició primària, deixarem els valors per defecte i per últim W per guardar.

![Imatge 01](IMA/ING4.png)

Comprovarem si s'ha creat correctament.

![Imatge 01](IMA/ING5.png)

Despres ficarem el format XFS amb aquesta comanda

![Imatge 01](IMA/ING6.png)

Crearem la carpeta /media/backup per despres muntar-la a la carpeta /dev/sdb1

![Imatge 01](IMA/ING7.png)

Ara el següent pas serà instal·lar Duplicity

![Imatge 01](IMA/ING8.png)

Després creem dos usuaris addicionals amb carpetes personals, que seran user1 i user2

![Imatge 01](IMA/ING9.png)

Per comprovar que s’han creat correctament farem

![Imatge 01](IMA/ING10.png)

Configurem la contrasenya dels usuaris

![Imatge 01](IMA/ING11.png)

Crearem arxius buits sense propòsit només perquè estiguin allà per poder fer la prova a la carpeta home de l’usuari

![Imatge 01](IMA/ING12.png)

El següent pas es fer la còpia de seguretat de la carpeta /home amb la següent comanda

![Imatge 01](IMA/ING13.png)

Comprovareem que s'ha creat correctamen

![Imatge 01](IMA/ING14.png)

Ara esborrarem els arxius per poder fer la restauració

![Imatge 01](IMA/ING15.png)

El següent serà fer la restauració del /home de l’usuari

![Imatge 01](IMA/ING16.png)

Després crearem un nou fitxer per fer una altra comprovació

![Imatge 01](IMA/ING17.png)

Farem una copia incrementalamb aquesta comanda

![Imatge 01](IMA/ING18.png)

Ara desmuntarem /media/backup

![Imatge 01](IMA/ING19.png)

Ara crearem un script amb bin/bash que farà la còpia completa de /home de l’usuari principal

![Imatge 01](IMA/ING20.png)

Després li donarem permisos d’execució perquè si no no podrem executar-lo

![Imatge 01](IMA/ING21.png)

Programem al cron com a root l’execució de l’script els diumenges a les 23:00

![Imatge 01](IMA/ING22.png)

creem un altre arxiu executable de bin/bash, que sigui l’incremental

![Imatge 01](IMA/ING23.png)

Donarem també els permisos amb chmod.

![Imatge 01](IMA/ING24.png)

Comprovem que s'han creat correctament

![Imatge 01](IMA/ING25.png)

Executem el programa cron per configurar que es repeteixi a les 23 hores
