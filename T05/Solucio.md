# SSH

![Imatge 01](IMG/WW1.png)
![Imatge 01](IMG/WW5.png)

Primer configurem l’adaptador de xarxa, i posem un en NAT i l’altre en adaptador només amfitrió, en les dues màquines.

![Imatge 01](IMG/WW6.png)

Modifiquem l’arxiu Netplan.

![Imatge 01](IMG/WW7.png)
![Imatge 01](IMG/WW8.png)

Seguidament instal·larem l’SSH i comprovarem l’estat del servei.

![Imatge 01](IMG/WW9.png)

Necessitarem fer ip a per mirar les IP.

![Imatge 01](IMG/WW10.png)

Per connectar-nos via SSH haurem de posar el nom de l’usuari i, al costat, la seva IP, però haurem de posar la IP de l’adaptador amfitrió.

![Imatge 01](IMG/WW11.png)

Aquesta comanda és merament per comprovar que estem a l’usuari.
![Imatge 01](IMG/WW12.png)

Per habilitar l’usuari root, haurem d’activar-lo mitjançant la comanda sudo passwd root, que li assignarà una contrasenya.
![Imatge 01](IMG/WW13.png)

I després modificarem l’arxiu sshd_config, mitjançant la comanda  
sudo nano /etc/ssh/sshd_config i afegirem AllowUsers usuari.

![Imatge 01](IMG/WW14.png)
Després comprovarem si l’usuari pot fer login com a local, però no pot iniciar sessió via SSH. Primer iniciarem sessió com a root en la màquina Ubuntu.

![Imatge 01](IMG/WW15.png)

Després intentarem iniciar sessió com a usuari root i veurem que ens denega l’accés.

![Imatge 01](IMG/WW16.png)

Després, a la màquina de Windows, amb la comanda ssh-keygen -t rsa generarem uns codis RSA.

![Imatge 01](IMG/WW17.png)

Ara haurem de veure que els arxius anteriors s’han creat.

![Imatge 01](IMG/WW18.png)

I els copiem a la màquina Ubuntu.

![Imatge 01](IMG/WW19.png)

Amb aquesta comanda, crearem un arxiu dintre de la carpeta.

![Imatge 01](IMG/WW20.png)

I copiarem la clau id_rsa dintre de l’arxiu que hem creat.

![Imatge 01](IMG/WW2.png)

Després anirem a Configuració i li donarem a Sistema.

![Imatge 01](IMG/WW3.png)

I seguidament a Característiques opcionals.

![Imatge 01](IMG/WW4.png)

Li donarem que sí.

![Imatge 01](IMG/WW21.png)

I en el buscador posarem Servidor OpenSSH.

![Imatge 01](IMG/WW22.png)

Li donarem a Afegir.

![Imatge 01](IMG/WW23.png)

I esperarem que s’afegeixi.

![Imatge 01](IMG/WW24.png)

Després buscarem l’apartat de Firewall.

![Imatge 01](IMG/WW25.png)

Li donarem a Xarxa pública.

![Imatge 01](IMG/WW26.png)

I desactivarem el Firewall.

![Imatge 01](IMG/WW27.png)

Després executarem el PowerShell com a administrador.

![Imatge 01](IMG/WW28.png)

Després iniciarem el servei.

![Imatge 01](IMG/WW29.png)

I farem que cada cop que s’iniciï la màquina, s’activi el servei.

![Imatge 01](IMG/WW30.png)

Aquesta comanda la realitzarem per veure la IP de l’adaptador només amfitrió, i ens connectarem a la màquina Ubuntu.

![Imatge 01](IMG/WW31.png)

Ara, per realitzar la pràctica, primer farem un ping per comprovar que es veuen les màquines.

![Imatge 01](IMG/WW32.png)

I ens connectarem a la màquina de Windows realitzant la mateixa comanda, només que posant el nom i la IP de l’altra màquina.

![Imatge 01](IMG/WW33.png)

I amb la següent comanda crearem un túnel.

![Imatge 01](IMG/WW34.png)

![Imatge 01](IMG/WW35.png)

Ara configurarem el túnel que hem creat, entrant al Panell de Control.

![Imatge 01](IMG/WW36.png)

On entrarem a Xarxes i Internet.

![Imatge 01](IMG/WW37.png)

Després a Opcions d’Internet.

![Imatge 01](IMG/WW38.png)

Després a Connexions i a Configuració LAN.

![Imatge 01](IMG/WW39.png)

Després haurem d’activar la part de “usar un servidor proxy per la LAN”.

![Imatge 01](IMG/WW40.png)

I configurarem els SOCKS.

![Imatge 01](IMG/WW41.png)

Per últim, després d’instal·lar el Wireshark, que és tan fàcil com donar-li a descarregar per Windows, a la seva pàgina web, validarem el túnel, i ja ens hauria de sortir.

[torna al enunciat](README.md)

