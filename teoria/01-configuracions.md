# Configuracions: git config
Usat per establir una configuració específica d'usuari, com ara el correu electrònic, nom d'usuari i tipus de format, etc.:
```
git config --global user.name “nom cognom”
```
Serà el nom que utilitzarà per identificar l’autor i/o commiter dels comits realitzats.
```
git config --global user.email “valid-email”
```
Serà el email que utilitzarà per identificar l’autor i/o commiter dels comits realitzats. Per a una bona integració amb github és recommanable que aquest sigui el mateix
```
git config --global color.ui auto
```
Especificar un codi de colors automàtic per tal de que la sortida per pantalla de les ordres de git siguin fàcils de llegir i identificar.  
Fixa't que l’opció --global indica que aquestes configuracions seran valides per a tots els repositoris que presents i futurs que tens en el ordinador. Si per un repositori específic vols canviar alguna d’aquestes opcions, ves al directori de treball d’aquest projecte git (dintre el teu ordinador) i executa les ordres de git config amb l’opció --local:
```
git config --local user.name “nom2 cognom2”
```
Finalment si vols visualitzar les configuracions fetes, fés:
```
git config --list
```
