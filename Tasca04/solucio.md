# GUIA-SERVEIS DE DIRECTORI. LDAP

| 1. Requeriments d'Infraestructura Inicial |
|----------------------------------------|

- Configurem la màquina Server (Server Hostname), posem la següent comanda i després posem com a nom del host: server i com a nom del host complet: server.innovatechXX.test (XX, número de llista, 21).

![Configurant màquina virtual, adaptador 1 en NAT](img/Imatge01.png)

![Instal·lant la nostra eina, Bitwarden](img/Imatge02.png)

- Fem la comprovació amb: hostname i hostname -f.

![Instal·lant la nostra eina, Bitwarden](img/Imatge03.png)

- Adaptador 1 de xarxa en NAT, el posem/deixem en NAT.

![Instal·lant la nostra eina, Bitwarden](img/Imatge04.png)

- Posem l'adaptador 2 de xarxa en Adaptador de només amfitrió, per a la comunicació privada amb el Client virtual  i la màquina física.

![Instal·lant la nostra eina, Bitwarden](img/Imatge05.png)

- Escrivim: ip a, per veure les IP’s.

![Instal·lant la nostra eina, Bitwarden](img/Imatge06.png)

| 2. Tasques d'Implementació i Configuració del Servidor LDAP |
|----------------------------------------|

| 2.1. Instal·lació i Configuració Base d'OpenLDAP |
|----------------------------------------|

- Instal·lem el servei OpenLDAP amb la següent comanda:

![Instal·lant la nostra eina, Bitwarden](img/Imatge07.png)

- Contrasenya: usuari. Continuem.

![Instal·lant la nostra eina, Bitwarden](img/Imatge08.png)

- Fem la comprovació, amb status.

![Instal·lant la nostra eina, Bitwarden](img/Imatge10.png)

- Posem la següent comanda per veure les dades del directori LDAP.

![Instal·lant la nostra eina, Bitwarden](img/Imatge11.png)

- Configuració de la base de dades, reconfigurem el paquet.

![Instal·lant la nostra eina, Bitwarden](img/Imatge09.png)

- Ens diu que no es crearà la configuració ni la base de dades inicial si habilitem aquesta opció, li diem que no volem ometre la configuració del servidor OpenLDAP.

![Instal·lant la nostra eina, Bitwarden](img/Imatge12.png)

- Deixem el nom de domini DNS com a predeterminat.

![Instal·lant la nostra eina, Bitwarden](img/Imatge13.png)



[Anar a l'enunciat](../Tasca04/README.md)  
[Anar a la pàgina inicial](../README.md)
