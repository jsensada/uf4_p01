# Branques: git branch / checkout / merge
Quan treballes en col·laboració, moltes vegades és habitual separar el treball en branques, és a dir, “temporalment” separar l’historial de canvis del projecte per realitzar uns canvis concrets i posteriorment, ajuntar-los de nou amb un merge.
Per crear una branca nova a partir del commit actual, utilitza:
```
git branch nom-branca
```
Si vols llistar totes les banques actuals del projecte:
```
git branch
```
Com que existeix la possibilitat de que el projecte hagi estat clonat i tingui un altre origen, utilitza -a per llistar les branques remotes i les locals:
```
git branch -a
```
Si el que vols és eliminar-ne una:
git branch -d nom-branca
Si pel contrari el que vols és canviar-te de branca:
```
git checkout nom-branca
```
Amb l'opció checkout pots crear una nova branca i a més canviar-te automàticament:
```
git checkout -b nom-branca
```
Existeixen moltes opcions de git pel que fa al treball en branques però ara mateix només ens fixarem en aquestes. Finalment tenim merge, aquesta ordre s’utilitza per fusionar una tots els commits d’una branca amb la branca actual:
```
git merge nom-branca2
```
Si només vols importar el contingut de la branca 2 com si fos un sol commit pots utilitzar:
```
git merge --squash nom-branca2  
```
