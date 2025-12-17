## T06: Accés remot. Escriptori remot (RDP)

![Imatge 01](INTE/INA1.png)
![Imatge 01](INTE/INA2.png)


Primer de tot haurem de configurar les 2 màquines tant Ubuntu com Windows en xarxa nat,

![Imatge 01](INTE/INA3.png)

Després en entrar a Windows anirem a configuració, a l’apartat de sistema i activarem escriptori remot, i entrem a Usuaris d'Escriptori Remot per a dir-li a la màquina quin usuari podrà connectar-se remotament.

![Imatge 01](INTE/INA4.png)

Li donarem a agregar

![Imatge 01](INTE/INA5.png)

Aquí hem de posar el mateix que apareix a l’apartat des d’aquesta ubicació, això s’escriu on diu escriviu els noms d’objecte que voleu seleccionar, afegint-hi una barra i el nom de l’usuari de la màquina Windows.

![Imatge 01](INTE/INA6.png)

Li donarem a acceptar

![Imatge 01](INTE/INA7.png)

I ja ens apareix als usuaris d’escriptori remot

![Imatge 01](INTE/INA8.png)

Després desactivarem el firewall

![Imatge 01](INTE/INA9.png)

Un cop iniciada la màquina Zornin, anirem a configuració i a l’apartat d’escriptori remot,

![Imatge 01](INTE/INA10.png)

I activarem les dues opcions.

![Imatge 01](INTE/INA11.png)

Mirarem la IP de la nostra màquina de Windows amb ipconfig

![Imatge 01](INTE/INA12.png)

Després obrirem l’aplicació d’escriptori remot de Linux que és remmina

![Imatge 01](INTE/INA13.png)

Aquí només li hem de donar a què si

![Imatge 01](INTE/INA14.png)

Posarem el nom i la contrasenya de Windows, i li donarem a acceptar

![Imatge 01](INTE/INA15.png)

I ja estaria, ja ens podríem connectar a la màquina de Windows.

![Imatge 01](INTE/INA16.png)

Després a la màquina de Windows, posarem l’IP de la nostra màquina de Zornin a la seva aplicació d’escriptoris remots.

![Imatge 01](INTE/INA17.png)

I haurem d'recordar-nos del nom d’usuari i la contra de la màquina Zornin.

![Imatge 01](INTE/INA18.png)

I aquí posarem les dades mencionades anteriorment.

![Imatge 01](INTE/INA19.png)

I ja tindríem accés des de Zornin a Windows.

