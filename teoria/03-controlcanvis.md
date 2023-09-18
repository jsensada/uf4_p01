# Control de canvis: git status / diff / add / reset / commit
Una vegada tens un projecte inicilitzat en el teu directori de treball, pots començar a treballar i a registrar activitat i canvis. Amb git status tindràs una idea dels fitxers que han canviat des de l’inicialització o últim commit registrat:
```
git status
```
Amb aquesta informació podràs veure quins han estat els fitxers que han canviat, si han estat modificats, creats o eliminats. Tingues en compte que git només treballa amb fitxers, mai amb directoris. Git no registrarà que has crear un directori nou, només quan hi hagi algun fitxer a dintre.
Si el que vols és fer una diferència respecte l'últim commit, pots utilitzar diff:
```
git diff
```
Recorda que perquè diff mostri els canvis, aquests fitxers han d’haver estat alguna vegada afegits i comitejats. Si no, és incapaç de poder comprovar les diferències. Per afegir fitxers al index utilitzarem:
```
git add “path”
```
Amb add li has d’especificar la ruta dels fitxers que vols afegir:
```
git add nom-fitxer.txt
```
Si del contrari vols afegir tot un directori:
```
git add path/
```
Si estas dintre un directori i vols afegir tots els canvis que has fet en aquest directori (ja sigui eliminar, crear o modificar), fés servir la ordre:
```
git add .
```
Si pel que sigui la ruta inicial de projecte és path/directori1 i actualment et trobes a la ruta path/directori1/directori2 i vols afegir canvis que has realitzats en el path/directori3, no cal que et canvis de ruta, pots utilitzar el path relatiu:
```
git add ../directori3
```
O també pots afegir tots els canvis realitzats en qualsevol dels fitxers del projecte:
```
git add --all
gti add -A
```
Les dos ordres anteriors són equivalents. Si pel que sigui necessites eliminar algun fitxer de l'índex és a dir, no el vols incloure en el següent commit, pots utilitzar:
```
git restore --staged “nom-fitxer”.txt
```
La ordre anterior en cap cas modificarà el contingut del fitxer, només s'eliminarà de l'índex i el següent commit no afegeix els canvis realitzats en el fitxer “nom-fitxer”.txt. Si el que busques és restablir els canvis realitzats en el fitxer des de l'últim commit, fés:
```
git reset
```
Amb reset podràs tenir múltiples opcions que ja explorarem més endavant.
Una vegada tens el index de fitxers que vols registrar com a canviats (creat amb git add) ja podràs crear el commit. La manera més senzilla de crear el commit és:
```
git commit -m “breu missatge identificatiu del canvi”
```
Si no has realitzat cap git add i vols afegir tots els canvis directament pots fer el commit amb l'opció -am:
```
git commit -am “breu missatge identificatiu del canvi”
```
