# 🐧 Cerințe workflow GitHub Actions – Linux Training

## 📌 Specificații generale

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
