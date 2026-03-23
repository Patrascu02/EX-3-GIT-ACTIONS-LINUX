# 🐧 Cerințe workflow GitHub Actions – Linux Training + Auto Branch Push + System Report Artifact

---

## 1) 🔹 Linux Training

### 📌 Specificații generale

* **Nume workflow:** la alegere (ex: `Linux-Training`)
* **Declanșator:** manual (`workflow_dispatch`)
* **Input:**

  * `nume_utilizator` (obligatoriu)
* **Sistem de operare:** `ubuntu-latest`

---

## ⚙️ Pași necesari

### Pasul 1

Afișează în log-uri data și ora curentă a sistemului.

### Pasul 2

Afișează mesajul:

```
Salutare, [nume_utilizator]! Începem antrenamentul Linux.
```

### Pasul 3

Creează un director numit `date_sistem`.

### Pasul 4

Creează un fișier `info.txt` în directorul `date_sistem` cu textul:

```
Acest fișier a fost generat automat de GitHub Actions.
```

### Pasul 5

Afișează în log-uri conținutul directorului `date_sistem`.

### Pasul 6

Afișează în log-uri conținutul fișierului `info.txt`.

---

## 2) 🔹 Auto Branch & Push

### 📌 Specificații generale

* **Nume workflow:** la alegere (ex: `Auto-Branch-Push`)
* **Declanșator:** manual (`workflow_dispatch`)
* **Inputs (obligatorii):**

  * `nume_branch` (ex: `update-automat`)
  * `mesaj_commit` (ex: `Adaug raport nou`)
* **Sistem de operare:** `ubuntu-latest`

---

## ⚙️ Pași necesari

### Pasul 1

Aduce codul pe mașina virtuală.

### Pasul 2

Configurează identitatea Git (user.name și user.email).

### Pasul 3

Creează și comută pe branch-ul nou folosind valoarea din `nume_branch`.

### Pasul 4

Creează un fișier `raport-automat.txt` cu conținutul:

```
Acest fișier a fost creat pe branch-ul [nume_branch]
```

### Pasul 5

Adaugă și dă commit fișierului folosind mesajul din input-ul `mesaj_commit`.

### Pasul 6

Fă push la branch-ul nou creat către repository-ul remote.

---

## 3) 🔹 System Report Artifact

### 📌 Specificații generale

* **Nume workflow:** la alegere (ex: `System-Report-Artifact`)
* **Declanșator:** manual (`workflow_dispatch`)
* **Sistem de operare:** `ubuntu-latest`
* **Input:** nu necesită

---

## ⚙️ Pași necesari

### Pasul 1

Aduce codul pe mașina virtuală.

### Pasul 2

Creează un folder pentru rapoarte numit `date_extrase`.

### Pasul 3

Rulează comenzi Linux pentru a investiga sistemul și salvează rezultatele într-un fișier `raport_server.txt` în folderul `date_extrase`:

* Scrie un titlu simplu
* Află ce sistem de operare rulează
* Află câtă memorie RAM are calculatorul
* Află cât spațiu pe hard-disk există
* Află detalii despre procesor (CPU)

### Pasul 4

Salvează folderul `date_extrase` ca artefact utilizabil în GitHub Actions pentru descărcare.

* Nume artefact: la alegere (ex: `Raportul-Meu-Secret`)
* Cale artefact: `date_extrase/`
