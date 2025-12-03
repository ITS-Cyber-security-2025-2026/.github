🔐 Tutorial: Installazione Git + Configurazione SSH

Se non sai come installare Git o configurare SSH, segui questa guida semplice.

💻 1. INSTALLAZIONE DI GIT
🪟 Windows

Apri PowerShell e scrivi:

winget install --id Git.Git -e --source winget


Chiudi e riapri PowerShell, poi verifica l’installazione:

git --version


Se vedi qualcosa tipo:

git version 2.xx.x


Git è installato correttamente.

🐧 Linux (Ubuntu / Debian / Kali / Mint)

Apri Bash e scrivi:

sudo apt update
sudo apt install git


Verifica:

git --version

⚙️ 2. COMANDI BASE DI GIT
📥 Per scaricare una repository (clone)
git clone git@github.com:ITS-Cyber-security-2025-2026/nomerepo.git

📤 Per inviare modifiche su GitHub

Dentro la cartella della repo:

git add .


✔️ Aggiunge tutti i file modificati alla staging area

git commit -m "descrizione della modifica"


✔️ Crea un commit con un messaggio

git push


✔️ Invii le modifiche su GitHub

🔑 3. SETUP DELLA CHIAVE SSH
🧪 Genera la chiave SSH

Apri PowerShell e scrivi:

ssh-keygen -t ed25519 -C "la.mail@che.usisugit.com"


Quando appare:

Enter a file in which to save the key:


Premi INVIO senza modificare nulla.

📄 Visualizza la chiave pubblica
cat ~/.ssh/id_ed25519.pub


Il testo mostrato è la tua chiave SSH pubblica.
Copiala completamente.

🔗 Aggiungi la chiave al tuo account GitHub

Vai su GitHub (browser)

Clicca in alto a destra sul tuo profilo

Settings

SSH and GPG keys

New SSH key

Incolla la chiave copiata

Lascia Authentication Key

Dai un nome (es. “PC personale”)

Salva

🎉 Tutto fatto!

Ora puoi usare Git senza password e lavorare con tutte le repository dell’organizzazione.
