# FONAMENTS DEL SERVEI DNS

Posem el 2 adaptador en adaptador pont, després dins de la màquina, anem a configuració, xarxa, Ethernet (enp0s8), afegim, posem la direcció, màscara de xarxa i guardem.

![Posant Server Hostname](img/Imatge02.png)

![Posant Server Hostname](img/Imatge01.png)

## Identifica la IP de resposta, el valor TTL i el servidor que ha respost a la consulta.
- **IP de resposta:** 83.247.151.214  
- **Valor TTL:** 243 segons  
- **Servidor que ha respost:** 127.0.0.53 (resolent a través de UDP)

![Posant Server Hostname](img/Imatge03.png)

## Quins són els servidors de noms autoritatius per a aquest domini?
Els servidors de noms autoritatius per al domini tecnocampus.cat són:
- ns-1071.awsdns-05.org
- ns-130.awsdns-16.com
- ns-1689.awsdns-19.co.uk
- ns-535.awsdns-02.net

![Posant Server Hostname](img/Imatge04.png)

![Posant Server Hostname](img/Imatge05.png)

## Quina és la informació del correu de l'administrador i el número de sèrie del domini?
El correu de l’administrador mostra qui és el responsable tècnic del domini.     
**Correu de l’administrador:** root@dns1.nominalia.com    
           **Número de sèrie:** 1761028965

![Posant Server Hostname](img/Imatge06.png)

![Posant Server Hostname](img/Imatge07.png)

## Quina informació sobre els registres s’obté?
S’obtenen diversos registres PTR associats a la IP 147.83.2.135.
Que aquests apunten a dominis de la UPC (Universitat Politècnica de Catalunya).
Registres obtinguts:       
**- barcelonatech-upc.eu**           
**- www.upc.es**     
**- saladepremsa.upc.edu**     
**- edicioweb.produccio.upc.edu**    
**- masters.upc.edu**   
**- upc.cat**   
**- barcelonatech.upc.edu**   
**- upc.edu**

![Posant Server Hostname](img/Imatge08.png)

![Posant Server Hostname](img/Imatge09.png)



[Anar a l'enunciat](../Tasca06/README.md)  
[Anar a la pàgina inicial](../README.md)
