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

Posem contrasenya als 2 usuaris.

![Posem contrasenya als 2 usuaris.](img/Imatge466.png)

![Posem contrasenya als 2 usuaris.](img/Imatge467.png)

| 4. Integració de Client (Client Ubuntu Desktop) |
|----------------------------------------|

Instal·lem el client i configurem la interfície de xarxa, deixem l’adaptador 1 en NAT i posem el segon en adaptador de només l’amfitrió, seguidament després comprovem amb ip a, tot això per comunicar-se amb el servidor.

![Instal·lem el client i configurem la interfície de xarxa, deixem l’adaptador 1 en NAT i posem el segon en adaptador de només l’amfitrió, seguidament després comprovem amb ip a, tot això per comunicar-se amb el servidor.](img/Imatge47.png)

![Instal·lem el client i configurem la interfície de xarxa, deixem l’adaptador 1 en NAT i posem el segon en adaptador de només l’amfitrió, seguidament després comprovem amb ip a, tot això per comunicar-se amb el servidor.](img/Imatge48.png)

![Instal·lem el client i configurem la interfície de xarxa, deixem l’adaptador 1 en NAT i posem el segon en adaptador de només l’amfitrió, fem actualitzacions i seguidament després comprovem amb ip a, tot això per comunicar-se amb el servidor.](img/Imatge50.png)

Fem clic a la barra, en surten diverses opcions, escollim Instantànies, després, cliquem on posa + fes, guardem els canvis i iniciem la màquina.

![Instantània.](img/Imatge49.png)

Primer fem actualitzacions.

![Actualitzacions](img/Imatge53.png)

![Actualitzacions](img/Imatge54.png)

Després ip a, per veure la ip i posar-la.

![Ip a](img/Imatge55.png)

Configurem l'arxiu d'hosts del client per resoldre l'adreça IP del servidor a server.innovatechXX.test. Primer posem la següent comanda per entrar a l’arxiu /etc/hosts

![Entrem en /etc/hosts](img/Imatge51.png)

Canviem la segona i tercera línea, amb l’ip, innovatech.test

![Configurem l'arxiu d'hosts del client per resoldre l'adreça IP del servidor a server.innovatech21.test.](img/Imatge522.png)

Després anem a l’arxiu /etc/hostname

![Anem a l’arxiu /etc/hostname](img/Imatge56.png)

On posem client.innovatech21.test

![Posem client.innovatech21.test](img/Imatge57.png)

Fem la comprovació.

![Comprovació de configuració de l'arxiu d'hosts del client per resoldre l'adreça IP del servidor a server.innovatechXX.test.](img/Imatge58.png)

![Comprovació de configuració de l'arxiu d'hosts del client per resoldre l'adreça IP del servidor a server.innovatechXX.test.](img/Imatge599.png)

Ara primerament comencem instal·lant els mòduls necessaris per permetre l'autenticació amb LDAP. Instal·lem els mòduls necessaris per usar libmap i nss.

![Instal·lem els mòduls necessaris per permetre l'autenticació amb LDAP. Instal·lem els mòduls necessaris per usar libmap i nss.](img/Imatge60.png)

Posem l’identificador uniforme de recursos del servidor LDAP.

![Posem l’identificador uniforme de recursos del servidor LDAP.](img/Imatge61.png)

Posem el nom distingit de la base de cerca.

![Posem el nom distingit de la base de cerca.](img/Imatge62.png)

Posem la versió LDAP a utilitzar, 3.

![Posem la versió LDAP a utilitzar, 3.](img/Imatge63.png)

Fes que l'usuari root local sigui administrador de la base de dades, posem que si.

![Fes que l'usuari root local sigui administrador de la base de dades, posem que si.](img/Imatge64.png)

Ens diu que, si la base de dades LDAP requereix login, posem que no.

![Ens diu que, si la base de dades LDAP requereix login, posem que no.](img/Imatge65.png)

Posem el compte LDAP per a l'usuari root.

![Posem el compte LDAP per a l'usuari root.](img/Imatge66.png)

Posem la contrasenya del compte root LDAP.

![Posem la contrasenya del compte root LDAP.](img/Imatge67.png)

![Instal·lem els mòduls necessaris per permetre l'autenticació amb LDAP. Instal·lem els mòduls necessaris per usar libmap i nss.](img/Imatge68.png)

Ara comprovem la connectivitat amb el servidor fent una consulta ldapsearch des del client.

![Comprovem la connectivitat amb el servidor fent una consulta ldapsearch des del client.](img/Imatge69.png)

![Comprovem la connectivitat amb el servidor fent una consulta ldapsearch des del client.](img/Imatge70.png)

Modifiquem els arxius de configuració del client necessaris. Primerament configurem l'arxiu nsswitch.conf, indicant que s'usarà ldap per usuaris i grups.

![Modifiquem els arxius de configuració del client necessaris. Primerament configurem l'arxiu nsswitch.conf, indicant que s'usarà ldap per usuaris i grups.](img/Imatge71.png)

![Modifiquem els arxius de configuració del client necessaris. Primerament configurem l'arxiu nsswitch.conf, indicant que s'usarà ldap per usuaris i grups.](img/Imatge72.png)

Canvis:

![Modifiquem els arxius de configuració del client necessaris. Primerament configurem l'arxiu nsswitch.conf, indicant que s'usarà ldap per usuaris i grups.](img/Imatge722.png)

Ara anem a l'arxiu /etc/pam.d/common-password, anem a aquesta línea que surt (sortia): use_authtok i eliminem: use_authtok

![Anem a l'arxiu /etc/pam.d/common-password, anem a aquesta línea que surt (sortia): use_authtok i eliminem: use_authtok](img/Imatge73.png)

![Anem a l'arxiu /etc/pam.d/common-password, anem a aquesta línea que surt (sortia): use_authtok i eliminem: use_authtok](img/Imatge74.png)

![Anem a l'arxiu /etc/pam.d/common-password, anem a aquesta línea que surt (sortia): use_authtok i eliminem: use_authtok](img/Imatge7444.png)

Ara anem a l’arxiu /etc/pam.d/common-session, on afegim la següent línia per crear els perfils.

![Anem a l’arxiu /etc/pam.d/common-session, on afegim la següent línia per crear els perfils.](img/Imatge75.png)

![Anem a l’arxiu /etc/pam.d/common-session, on afegim la següent línia per crear els perfils.](img/Imatge76.png)

Canvi:

![Anem a l’arxiu /etc/pam.d/common-session, on afegim la següent línia per crear els perfils.](img/Imatge766.png)

Reiniciem els serveis i verifiquem amb la següent comanda: getent passwd que els usuaris del directori són visibles localment.

Reiniciem el servei.

![Reiniciem el servei.](img/Imatge77.png)

![Reiniciem el servei.](img/Imatge78.png)

Comprovem que veu els usuaris LDAP.

![Comprovem que veu els usuaris LDAP.](img/Imatge79.png)

![Comprovem que veu els usuaris LDAP.](img/Imatge80.png)

Editem aquest arxiu amb la següent comanda:

![Editem aquest arxiu amb la següent comanda:](img/Imatge81.png)

Per permetre l’inici de sessió gràfica, afegint la següent línea.

![Per permetre l’inici de sessió gràfica, afegint la següent línea.](img/Imatge82.png)

![Per permetre l’inici de sessió gràfica, afegint la següent línea.](img/Imatge83.png)

Reiniciem el client i provem a iniciar sessió amb un dels usuaris del directori.

Anem a afegir un usuari, en aquest cas mostraré el tech01

![Anem a afegir un usuari, en aquest cas mostraré el tech01](img/Imatge84.png)

Posem el nom ttech01

![Posem el nom ttech01](img/Imatge85.png)

I la contrasenya.

![I la contrasenya.](img/Imatge86.png)

I ens entra.

![I ens entra.](img/Imatge87.png)

Usuaris del directori.

![Usuaris del directori.](img/Imatge88.png)

Després d’iniciar sessió, comprovem que se li ha creat la carpeta personal i comprovem l’usuari.

![Després d’iniciar sessió, comprovem que se li ha creat la carpeta personal i comprovem l’usuari.](img/Imatge89.png)


[Anar a l'enunciat](../Tasca04/README.md)  
[Anar a la pàgina inicial](../README.md)
