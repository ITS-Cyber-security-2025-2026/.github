# 🔐 Tutorial: Installazione di Git + Configurazione SSH

Se non sai come installare Git o configurare SSH, segui questa guida semplice e ordinata.

---

## 💻 1. Installazione di Git

### 🪟 Windows

Apri PowerShell e scrivi:

```bash
winget install --id Git.Git -e --source winget
```

Chiudi e riapri PowerShell, poi verifica l’installazione:

```bash
git --version
```

Se ottieni qualcosa tipo:

```
git version 2.xx.x
```

Allora Git è installato correttamente.

---

### 🐧 Linux (Ubuntu / Debian / Kali / Mint)

Apri Bash e scrivi:

```bash
sudo apt update
sudo apt install git
```

Verifica:

```bash
git --version
```

---

## ⚙️ 2. Comandi base di Git

### 📥 Clonare una repository

```bash
git clone git@github.com:ITS-Cyber-security-2025-2026/nomerepo.git
```

### 📤 Inviare modifiche su GitHub

All’interno della cartella della repo:

```bash
git add .
```
✔️ Aggiunge tutti i file modificati alla staging area

```bash
git commit -m "descrizione della modifica"
```
✔️ Crea un commit con un messaggio

```bash
git push
```
✔️ Invia le modifiche su GitHub

---

## 🔑 3. Setup della chiave SSH

### 🧪 Generare la chiave SSH

Apri PowerShell e scrivi:

```bash
ssh-keygen -t ed25519 -C "la.mail@che.usisugit.com"
```

Quando appare:

```
Enter a file in which to save the key:
```

Premi INVIO senza modificare nulla.

---

### 📄 Visualizzare la chiave pubblica

```bash
cat ~/.ssh/id_ed25519.pub
```

Copia tutto il testo mostrato: è la tua chiave SSH pubblica.

---

### 🔗 Aggiungere la chiave al tuo account GitHub

1. Vai su GitHub dal browser  
2. Clicca sul tuo profilo (in alto a destra)  
3. *Settings*  
4. *SSH and GPG keys*  
5. *New SSH key*  
6. Incolla la chiave  
7. Lascia selezionato: **Authentication Key**  
8. Dai un nome alla chiave (es. “PC personale”)  
9. Salva

---

## 🎉 Tutto fatto!

Ora puoi usare Git senza inserire password e lavorare con tutte le repository dell’organizzazione.
