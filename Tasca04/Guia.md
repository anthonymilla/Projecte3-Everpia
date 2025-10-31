# GUIA-SERVEIS DE DIRECTORI. LDAP

| 1. Requeriments d'Infraestructura Inicial |
|----------------------------------------|

Configurem la màquina Server (Server Hostname), posem la següent comanda i després posem com a nom del host: server i com a nom del host complet: server.innovatechXX.test (XX, número de llista, 21).

![Configurant màquina Server, posem el nom del host: server i com a nom del host complet: server.innovatechXX.test (XX, número de llista, 21).](img/Imatge01.png)

![Posant Server Hostname](img/Imatge02.png)

Fem la comprovació amb: hostname i hostname -f.

![Comprovació Server Hostname](img/Imatge03.png)

Adaptador 1 de xarxa en NAT, el posem/deixem en NAT.

![Adaptador 1 de xarxa en NAT, el posem/deixem en NAT.](img/Imatge04.png)

Posem l'adaptador 2 de xarxa en Adaptador de només amfitrió, per a la comunicació privada amb el Client virtual  i la màquina física.

![Posem l'adaptador 2 de xarxa en Adaptador de només amfitrió](img/Imatge05.png)

Posem la següent comanda per habilitar el segon adaptador, apliquem els canvis i guardem els canvis.

![Posem la següent comanda per habilitar el segon adaptador, apliquem els canvis i guardem els canvis.](img/Imatge055.png)

![Posem la següent comanda per habilitar el segon adaptador, apliquem els canvis i guardem els canvis.](img/Imatge0555.png)

![Posem la següent comanda per habilitar el segon adaptador, apliquem els canvis i guardem els canvis.](img/Imatge05555.png)

Verifiquem, escrivim: ip a, per veure les IP’s.

![Verifiquem, escrivim: ip a, per veure les IP’s.](img/Imatge06.png)

| 2. Tasques d'Implementació i Configuració del Servidor LDAP |
|----------------------------------------|

| 2.1. Instal·lació i Configuració Base d'OpenLDAP |
|----------------------------------------|

Instal·lem el servei OpenLDAP amb la següent comanda:

![Instal·lant el servei OpenLDAP](img/Imatge07.png)

Contrasenya: usuari. Continuem.

![Posant la contrasenya](img/Imatge08.png)

Fem la comprovació, amb status.

![Posant la comanda status per fer la comprovació](img/Imatge10.png)

Posem la següent comanda per veure les dades del directori LDAP.

![Comanda per veure les dades del directori LDAP.](img/Imatge11.png)

Configuració de la base de dades, reconfigurem el paquet.

![Configuració de la base de dades, reconfigurem el paquet.](img/Imatge09.png)

Ens diu que no es crearà la configuració ni la base de dades inicial si habilitem aquesta opció, li diem que no volem ometre la configuració del servidor OpenLDAP.

![Configuració de slapd](img/Imatge12.png)

Posem de nom de domini DNS: innovatech21.test 

![Posant el nom de domini DNS](img/Imatge13.png)

Nom de la organització: innovatech21.test

![Nom de la organització](img/Imatge14.png)

Contrasenya de l’administrador, p@ssw0rd

![Contrasenya de l’administrador](img/Imatge15.png)

![Contrasenya de l’administrador](img/Imatge16.png)

Indiquem que quan s’elimini el paquet, s’esborri la BD creada.

![Indicant que quan s’elimini el paquet, s’esborri la BD creada.](img/Imatge17.png)

Movem la informació del directori que hi ha a una carpeta de backup.

![Movem la informació del directori que hi ha a una carpeta de backup.](img/Imatge18.png)

![Configuració de slapd](img/Imatge19.png)

Fem la comprovació de que s’ha modificat la informació del directori.

![Fem la comprovació de que s’ha modificat la informació del directori.](img/Imatge20.png)

Posem la següent comanda i creem dues OUs: users i groups mitjançant un fitxer .ldif.

![Posem la següent comanda i creem dues OUs: users i groups mitjançant un fitxer .ldif.](img/Imatge21.png)

![Posem la següent comanda i creem dues OUs: users i groups mitjançant un fitxer .ldif.](img/Imatge22.png)

Seguidament posem la següent comanda, per agregar l'arxiu al directori.

![Posem la següent comanda, per agregar l'arxiu al directori.](img/Imatge23.png)

Fem una consulta amb la comanda ldapsearch mostrant totes les OUs creades al directori.

![Fem una consulta amb la comanda ldapsearch mostrant totes les OUs creades al directori.](img/Imatge24.png)

| 3.2. Gestió i Administració (LAM) |
|----------------------------------------|

Instal·lem el Gestor d'Usuaris LDAP (LAM) amb la següent comanda, això ja descarregarà totes les dependències necessàries.

![Instal·lem el Gestor d'Usuaris LDAP (LAM) amb la següent comanda, això ja descarregarà totes les dependències necessàries.](img/Imatge25.png)

![Instal·lem el Gestor d'Usuaris LDAP (LAM) amb la següent comanda, això ja descarregarà totes les dependències necessàries.](img/Imatge26.png)

Posem ip a, per veure l'ip i després la posem al buscador agregant al final /lam i entrarem a la web.

![Posem ip a, per veure l'ip i després la posem al buscador agregant al final /lam i entrarem a la web.](img/Imatge27.png)

Dins, cliquem en LAM configuration.

![Cliquem en LAM configuration.](img/Imatge28.png)

Després Edit server profiles.

![Edit server profiles](img/Imatge29.png)

Posem la contrasenya; lam i entrem.

Manage server profiles: amb aquest pots administrar els diferents perfils, contrasenya..

![Posem la contrasenya; lam i entrem.](img/Imatge30.png)

Ara anem a opcions generals i configurem, compte, admin, idioma..

![Opcions generals i configurem, compte, admin, idioma..](img/Imatge31.png)

![Opcions generals i configurem, compte, admin, idioma..](img/Imatge32.png)

Anem a Account Types definim els DN dels usuaris i grups, també incloem una OU pels usuaris i una altre pels grups i es pot afegir els tipus d'objectes del directori, són usuaris i grups per defecte.

![Anem a Account Types definim els DN dels usuaris i grups, també incloem una OU pels usuaris i una altre pels grups i es pot afegir els tipus d'objectes del directori, són usuaris i grups per defecte.](img/Imatge33.png)

Accedim al directori.

![Accedim al directori.](img/Imatge34.png)

Ara creem els dos grups de seguretat al directori: tech i manager. Anem a comptes, grups i nou grup.

![Creem els dos grups de seguretat al directori: tech i manager. Anem a comptes, grups i nou grup.](img/Imatge35.png)

Primer grup.

![Primer grup](img/Imatge36.png)

Segon grup.

![Segon grup](img/Imatge37.png)

Ara creem un usuari per a cada grup: tech01 (membre de tech) i manager01 (membre de manager). Per els usuaris, anem a comptes, usuaris i nou usuari.

![Creem un usuari per a cada grup: tech01 (membre de tech) i manager01 (membre de manager). Per els usuaris, anem a comptes, usuaris i nou usuari.](img/Imatge38.png)

Primer usuari. Posem en personal el nom i cognom.

![Primer usuari. Posem en personal el nom i cognom.](img/Imatge39.png)

Després a Unix posem el nom de l'usuari i nom comú.

![Després a Unix posem el nom de l'usuari i nom comú.](img/Imatge40.png)

Ja està, s’ha creat un nou grup.

![S’ha creat un nou grup.](img/Imatge41.png)

Segon usuari. Posem en personal el nom i cognom.

![Segon usuari. Posem en personal el nom i cognom.](img/Imatge42.png)

Després a Unix posem el nom de l'usuari i nom comú.

![A Unix posem el nom de l'usuari i nom comú.](img/Imatge43.png)

Ja està, s’ha creat un nou grup.

![S’ha creat un nou grup.](img/Imatge44.png)

Ja estarien creats els grups.

![Ja estarien creats els grups.](img/Imatge45.png)

I ja estarien creats els usuaris.

![I ja estarien creats els usuaris.](img/Imatge46.png)

| 4. Integració de Client (Client Ubuntu Desktop) |
|----------------------------------------|





[Anar a l'enunciat](../Tasca04/README.md)  
[Anar a la pàgina inicial](../README.md)
