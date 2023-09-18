# Inicialització d’un projecte: git init / clone / remote
Amb l'ordre git init podeu inicialitzar un projecte de git en l’actual directori local de treball:
```
git init
```
Si el que voleu és que es crear un directori de treball nou i que aquest sigui un repositori de treball podeu fer:
```
git init “nom-projecte”
```
És recomanable que el nom del projecte no contingui espais ni caràcters especials ja que al final git treballa amb sistemes UNIX i la utilització de noms que no siguin alfanumèrics (a-z;A-Z;0-9) pot complicar el treball.
En el directori de treball on s’ha inicialitzat un projecte git, autimaticament s’haurà creat una carpeta oculta .git.
Existeix una altra manera de inicialitzar projectes git, fent un clon d’un projecte ja existent.
```
git clone “/path/projecte”
```
La ruta path del projecte farà un clon d’un projecte prèviament creat en un altre directori de treball de la màquina local. De totes maneres, normalment treballarem amb git per col·laborar amb altres persones. És per això que s’acostuma a allotjar els repositoris de git en plataformes web (públiques o privades). Alguns exemples són: Github, Gitlab, Bitbucket, etc. La forma en el qual treballarem serà, creant un repositori des del lloc web i després el clonarem a la nostra màquina:
```
git clone url
```
La connexió de git amb el repositori pot realitzar-se mitjançant HTTPS o SSH. És recomanable utilitzar SSH com a mètode de connexió. La url per SSH tindrà una forma semblant a:
```
git clone git@github.com:jsensada/example.git
```
Mentre que per https serà:
```
git clone https://github.com/jsensada/example.git
```
Una vegada hem realitzat el git clone, tindrem una nova carpeta example que contindrà tot el directori de treball del lloc remot així com la carpeta oculta .git que ens donarà informació de quin és l’origen del repositori. Per tant tindrem una versió en local del projecte, treballar-hi còmodament i podrem anar pujant els canvis cap a l’origen sense haver especificar-ho cada moment.
Pots comprovar quin és l’origen del repositori en cada moment mitjançant la ordre:
```
git remote -v
```
Amb git remote existeix una possibilitat de crear un repositori en local i posteriorment afegir-li l’origen remot. Això ho farem amb git remote:
```
git remote add origin git@github.com:jsensada/example.git
```