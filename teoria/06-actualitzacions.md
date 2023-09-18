# Compartir i actualitzar: git pull / git push
La comanda git pull s'utilitza per obtenir (git fetch) i fusionar (git merge) els canvis des d'un repositori remot al teu repositori local. Aquí tens els conceptes bàsics:
```
git pull
```
Quan executes git pull sense cap opció, git obtindrà els canvis del repositori remot configurat per a la teva branca actual i els fusionarà automàticament amb la teva branca local. Si vols obtenir i fusionar els canvis d'una branca específica al repositori remot, pots especificar el nom de la branca remota després de origin: 
```
git pull origin nom-branca2
```
Amb aquesta ordre, git obtindrà els canvis de la branca remota nom-branca  i els fusionarà amb la teva branca local actual nom-branca.
En lloc de fusionar els canvis del repositori remot, l'opció --rebase col·locarà els teus canvis locals sobre els canvis remots.
```
git pull --rebase
```
Això pot ajudar a mantenir un historial de commits més net i lineal.
La comanda git push s'utilitza per enviar els teus canvis locals al repositori remot:
```
git push origin nom-branca
```
Aquesta és la forma més comuna d'utilitzar git push.
Li diu a git que enviï els canvis de la teva branca local al repositori remot amb el nom especificat després de origin.
```
git push --all origin
```
Aquesta opció enviarà totes les branques locals al repositori remot. És útil quan vols enviar totes les teves branques alhora.
