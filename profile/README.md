## Download Git
[Scarica da qui](https://git-scm.com/downloads)

- Riavvia / apri un terminale, verifica con ` git --version `

```
git config --global user.name "nome cognome"
git config --global user.email "email usata su git"
```

- verifica con ` git config --global --list `


## Installare ed autenticarsi su GitHub CLI:

[Scarica da qui](https://cli.github.com/)

Poi da terminale: 
`git auth login`
##### Puoi saltare questo passaggio, Github ti chiede in automatico di identificarti quando serve

Scegliere:

GitHub.com
HTTPS
Login with browser

Alla fine verificare:

` git auth status `

## Scaricare una repository esistente

Se la repo esiste già su GitHub:
```
git clone https://github.com/FG-Stage/percorso-per-il-tuo-git.git
```

Poi entrare nella cartella: 

`cd tua-cartella-locale`

Controllare lo stato: 

`git status`

## Apportare modifiche a codice su git 
Serve a vedere quali file hanno ricevuto modifiche, aggiunte o rimozioni
`git status`

Aggiungere tutti i file modificati: 

`git add .`

Creare un commit: 

` git commit -m "testo bla bla" `

Caricare su GitHub: 

`git push`

Se è il primo push del branch: 

`git push -u origin main`

### Per non lavorare sul main, crea un branch
`git checkout -b [nome repo]/[nome nuovo branch]`

Poi lavorare normalmente:
```
git add .
git commit -m "Aggiunge pagina login"
git push -u origin feature/login-page
```

### Puoi cambiare branch così
`git branch`

Vedere anche i branch remoti:

`git branch -a`

Cambiare branch:

`git checkout nome-branch`

`git switch main`

## Se devi scaricare aggiornamenti da git
`git pull`

Se lavora su un branch specifico:

`git pull origin nome-branch`

## Vuoi creare una repo da terminale?
Prima accedi, poi può creare una repo privata e clonarla subito:

```
git repo create FG-stage/bla_bla --private --clone
```

Poi entra nella cartella:

`cd percorso locale`

Crea un README:

`echo "# Stage bla bla" > README.md`

Carica il primo commit:

```
git add .
git commit -m "Primo commit"
git push -u origin main
```

### Se invece vuoi creare nuova repo da progetto già esistente
Prima entra nel percorso del progetto con `cd`, poi invia:
```
gh repo create lFG-stage/nuovo_progetto --private --source=. --remote=origin --push
```
---
---
---
```
Valuta l'opzione di creare un .gitignore se necessario, non vogliamo caricare una repo online con tutti i pacchetti e librerie installate, no? Un requirements.txt per una .venv dovrebbe bastare, mentre per node si arrangia il packet manager.
```

Buona programmazione!
