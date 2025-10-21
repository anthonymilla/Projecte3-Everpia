# INFORME TÈCNIC: GESTORS DE CONTRASENYES

## 1. Introducció i Justificació  
Les contrasenyes febles, poc segures o reutilizades són un risc crític per a la seguretat de l’empresa, com:  
- Atacs de diccionari: Els atacants proven combinacions comunes de contrasenyes fins que troben una coincidència.  
- Credential stuffing: Si una contrasenya ha estat filtrada en un altre servei, pot ser reutilitzada per accedir a sistemes corporatius.  
- Accés no autoritzat: Pot exposar dades sensibles, comprometre sistemes i provocar pèrdues econòmiques.  

Un gestor de contrasenyes ajuda a mitigar aquests riscos ja què:  
- Genera contrasenyes fortes i úniques.  
- Emmagatzema les credencials de forma segura.  
- Facilita l’accés segur des de diferents dispositius.  
- Redueix la dependència de la memòria humana i evita l’ús de contrasenyes repetides.  

## 2. Comparativa Tècnica  
| Característica       | Bitwarden (Online/Núvol)             | KeePassX / KeePassXC (Offline / Escriptori) |
|---------------------|-----------------------------------|--------------------------------------------|
| Sincronització      | Automàtica entre dispositius via núvol | No disponible; cal copiar manualment l’arxiu |
| Seguretat           | Xifratge end-to-end amb clau mestra  | Xifratge local amb arxiu KDBX               |
| Accés multiplataforma | Web, mòbil, escriptori              | Només escriptori (portabilitat limitada)   |
| Model freemium / cost | Gratuït amb opcions premium          | Totalment gratuït i open source             |
| Dependència del núvol | Sí, cal connexió per sincronitzar   | No, totalment local                         |
| Portabilitat de l’arxiu | No aplica (gestió en núvol)         | Arxiu KDBX portable i exportable           |
| Codi obert           | Sí                                | Sí                                         |

## 3. Avantatges i Inconvenients  
- **Bitwarden (Online)**  
**Avantatges**:  
- Sincronització automàtica.  
- Accés des de qualsevol dispositiu.  
- Interfície intuïtiva.  

**Inconvenients**:  
- Dependència d’internet.  
- Risc potencial si el servidor és compromès (tot i el xifratge).  

- **KeePassX / KeePassXC (Offline)**  
**Avantatges**:  
- Control total de les dades.  
- No depèn de tercers ni connexió.  

**Inconvenients**:  
- Més complex de gestionar entre equips.  
- Risc de pèrdua si no es fa còpia de seguretat de l’arxiu.  

## 4. Recomanació  
Per al personal tècnic de l’empresa, es recomana **Bitwarden** com a gestor de contrasenyes principal. La seva capacitat de sincronització, el model de seguretat robust i la facilitat d’ús des de múltiples dispositius el fan ideal per a entorns professionals amb mobilitat i col·laboració. Aleshores KeePassXC pot ser útil com a complement en entorns molt sensibles o desconnectats, però no és tan pràctic per a l’ús diari en equip.


[Anar a l'enunciat](../Tasca01/README.md) [Anar a la pàgina inicial](../README.md)
