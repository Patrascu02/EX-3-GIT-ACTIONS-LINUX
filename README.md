# 🐧 Cerințe workflow GitHub Actions – Linux Training + Auto Branch Push

---

## 1) 🔹 Linux Training

### 📌 Specificații generale

* **Nume workflow:** la alegere (ex: `Linux-Training`)
* **Declanșator:** manual (`workflow_dispatch`)
* **Input:**

  * nume: `nume_utilizator`
  * obligatoriu (`required: true`)
* **Sistem de operare:** `ubuntu-latest`

---

## ⚙️ Pași necesari

### Pasul 1

Să afișeze în log-uri data și ora curentă a sistemului.

---

### Pasul 2

Să afișeze mesajul:

```
Salutare, [nume_utilizator]! Începem antrenamentul Linux.
```

(se va folosi valoarea introdusă în input)

---

### Pasul 3

Să creeze un director numit:

```
date_sistem
```

---

### Pasul 4

Să creeze un fișier:

```
date_sistem/info.txt
```

cu următorul conținut:

```
Acest fișier a fost generat automat de GitHub Actions.
```

---

### Pasul 5

Să afișeze în log-uri conținutul directorului `date_sistem`.

---

### Pasul 6

Să afișeze în log-uri conținutul fișierului `info.txt`.

---

# 2) 🔹 Auto Branch & Push

## 📌 Specificații generale

* **Nume workflow:** la alegere (ex: `Auto-Branch-Push`)
* **Declanșator:** manual (`workflow_dispatch`)
* **Inputs (obligatorii):**

  * `nume_branch` (ex: `update-automat`)
  * `mesaj_commit` (ex: `Adaug raport nou`)
* **Sistem de operare:** `ubuntu-latest`

---

## ⚙️ Pași necesari

### Pasul 1

Să aducă codul pe mașina virtuală folosind:

```
actions/checkout@v4
```

---

### Pasul 2

Să configureze identitatea Git:

```
git config user.name "GitHub Actions Bot"
git config user.email "bot@github.actions"
```

---

### Pasul 3

Să creeze și să se mute pe un branch nou folosind valoarea din `nume_branch`.

---

### Pasul 4

Să creeze un fișier:

```
raport-automat.txt
```

cu conținutul:

```
Acest fișier a fost creat pe branch-ul [nume_branch]
```

---

### Pasul 5

Să adauge și să dea commit fișierului:

```
git add .
git commit -m "[mesaj_commit]"
```

---

### Pasul 6

Să facă push la branch-ul nou creat către repository-ul remote (`origin`).
