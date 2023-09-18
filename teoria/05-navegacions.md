# Navegar en un projecte: git log / checkout
La ordre git log la utilitzaràs per revisar l'historial de canvis mentre que amb git checkout a més de permetre canviar de branques podràs moure's entre commits de l’historial.
```
git log
```
Aquesta comanda mostrarà l'historial de canvis en ordre cronològic invers, amb el commit més recent a dalt. Pots sortir de la vista d'historial prement la tecla “q”.
Aquesta ordre pot retornar-te una sortida per pantalla molt grossa, així que pots resumir-ho amb:
```
git log --oneline
```
Aquesta opció mostra cada commit en una sola línia, amb el resum del commit i el seu identificador abreviat. També pots visualitzar l’historial en forma de gràfic:
```
git log --graph
```
Aquesta opció mostra l'historial de canvis amb una representació gràfica dels branques i les fusions. És útil per veure la estructura del teu historial de canvis.
A part de visualitzacions genèriques, git log permet veure només els commits realitzats per un autor específic:
```
git log --author=nom-autor
```
De la mateixa manera si vols veure l'historial de canvis només per a un fitxer especificat, pots utilitzar aquesta comanda:
```
git log path/fitxer.txt
```
D’altra banda, una vegada consultat l’hisotrial, la comanda git checkout et permet canviar el teu directori de treball (working directory) i l'estat del teu repositori a un commit específic:
```
git checkout identificador-de-commit
```
Aquesta comanda et mourà al commit amb l'identificador especificat. Com ja s’ha dit, si el que vols és canviar a l'últim commit d’una branca determinada:
```
git checkout nom-de-branca
```
Això et serveix per repassar la teoria que els noms de branques són enllaços de tipus refs/branches/ a identificadors de commits.
De la mateixa manera que cd - en linux et porta al directori de treball anterior, amb checkout pots fer el mateix però per canviar de branques:
```
git checkout -
```
La comanda checkout, també pot ser utilitzada per restaurar fitxers del directori de treball a l’estat que estava en un commit determinat:
```
git checkout nom-de-fitxer.txt
```
Si no especifica el identificador del commit, agafarà l’últim commit de la branca, ara bé, git permet restaurar a qualsevol commit de l’historial:
```
git checkout nom-de-fitxer.txt identificador-de-commit
```
Recordeu que utilitzar `git checkout` pot canviar el teu directori de treball i l'estat del teu repositori, així que assegura't de fer-ho amb compte i fer còpies de seguretat dels canvis importants abans d'executar aquestes comandes, si cal.
