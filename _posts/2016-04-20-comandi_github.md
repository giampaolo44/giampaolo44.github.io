# Comandi Git da terminale

## Modifica a mano di alcune cose e seguente push su github

### Si va sulla cartella del blog e si scarica la versione corrente
`cd /home/giampaolo/blog-g44/`  
`git checkout master` --> se non sono su master, mi mette sulla master (per prudenza)  
`git pull origin master` --> aggiornare la versione locale con la versione del server - sincronizza DAL server  

### ....faccio delle modifiche (**dopo aver fatto la pull altrimenti rischio grossi casini/conflitti**)

`git status` --> verifico le modifiche che ho fatto ma non ho registrato che vedo in rosso  
`git add .`  --> preparazione per il commit di tutta la cartella ("."), altrimenti potrei dargli i singoli file o i percorsi da modificare  

Si potrebbero anche usare:

* `git rm <path>` --> fa il contrario: prepara alla rimozione roba che non serve più
* `git add -A` --> fa sia aggiungi che rimuovi, ma di tutte le modifiche fatte nel repo (come se usassi ".")

### Dopo aver completato le modifiche:
`git status`  --> verifico le modifiche che ho fatto -- fa vedere in verde le modifiche che ho registrato, in rosso se non le ho registrate
`git commit -m "descrizione modifiche"` --> faccio effettivamente il commit delle modifiche, di cui git fa uno snapshot che le rende pronte al push
`git push origin master` --> sincronizza VERSO il server

