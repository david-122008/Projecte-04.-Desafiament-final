# SSH

Primer configurem l’adaptador de xarxa, i posem un en NAT i l’altre en adaptador només amfitrió, en les dues màquines.

Modifiquem l’arxiu Netplan.

Seguidament instal·larem l’SSH i comprovarem l’estat del servei.

Necessitarem fer ip a per mirar les IP.

Per connectar-nos via SSH haurem de posar el nom de l’usuari i, al costat, la seva IP, però haurem de posar la IP de l’adaptador amfitrió.

Aquesta comanda és merament per comprovar que estem a l’usuari.

Per habilitar l’usuari root, haurem d’activar-lo mitjançant la comanda sudo passwd root, que li assignarà una contrasenya.

I després modificarem l’arxiu sshd_config, mitjançant la comanda  
sudo nano /etc/ssh/sshd_config i afegirem AllowUsers usuari.

Després comprovarem si l’usuari pot fer login com a local, però no pot iniciar sessió via SSH. Primer iniciarem sessió com a root en la màquina Ubuntu.

Després intentarem iniciar sessió com a usuari root i veurem que ens denega l’accés.

Després, a la màquina de Windows, amb la comanda ssh-keygen -t rsa generarem uns codis RSA.

Ara haurem de veure que els arxius anteriors s’han creat.

I els copiem a la màquina Ubuntu.

Amb aquesta comanda, crearem un arxiu dintre de la carpeta.

I copiarem la clau id_rsa dintre de l’arxiu que hem creat.

Després anirem a Configuració i li donarem a Sistema.

I seguidament a Característiques opcionals.

Li donarem que sí.

I en el buscador posarem Servidor OpenSSH.

Li donarem a Afegir.

I esperarem que s’afegeixi.

Després buscarem l’apartat de Firewall.

Li donarem a Xarxa pública.

I desactivarem el Firewall.

Després executarem el PowerShell com a administrador.

Després iniciarem el servei.

I farem que cada cop que s’iniciï la màquina, s’activi el servei.

Aquesta comanda la realitzarem per veure la IP de l’adaptador només amfitrió, i ens connectarem a la màquina Ubuntu.

Ara, per realitzar la pràctica, primer farem un ping per comprovar que es veuen les màquines.

I ens connectarem a la màquina de Windows realitzant la mateixa comanda, només que posant el nom i la IP de l’altra màquina.

I amb la següent comanda crearem un túnel.

Ara configurarem el túnel que hem creat, entrant al Panell de Control.

On entrarem a Xarxes i Internet.

Després a Opcions d’Internet.

Després a Connexions i a Configuració LAN.

Després haurem d’activar la part de “usar un servidor proxy per la LAN”.

I configurarem els SOCKS.

Per últim, després d’instal·lar el Wireshark, que és tan fàcil com donar-li a descarregar per Windows, a la seva pàgina web, validarem el túnel, i ja ens hauria de sortir.

