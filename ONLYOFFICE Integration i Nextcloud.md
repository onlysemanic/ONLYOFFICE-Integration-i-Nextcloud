# ONLYOFFICE-Integration i Nextcloud-guide

Følg denne vejledning for at integrere ONLYOFFICE i Nextcloud

---

## 1. Tilgå local.json-filen:

```bash
sudo nano /etc/onlyoffice/documentserver/local.json
```

---

## 2. Generer en hemmelig nøgle til secret.browser.string:

```bash
      "secret": {
        "browser": {
          "string": "<nøgle>"
        "inbox": {
          "string": "<nøgle>"
        "outbox": {
          "string": "<nøgle>"
        "session": {
          "string": "<nøgle>"
```

---

## 3. Genstart ds-converter og ds-docservice:

```bash
sudo systemctl restart ds-docservice 
sudo systemctl restart ds-converter
```

---

## 4. Gennemtjek om ds-converter og ds-docservice er aktive

```bash
sudo systemctl status ds-*
```

---

## 5. Åben Nextcloud og integrer ONLYOFFICE

Tilgå Nextcloud.
Vælg "Udvalgte Apps".
Find "ONLYOFFICE".
Download og aktivér ONLYOFFICE.
Vælg "Systemindstillinger".
Vælg "ONLYOFFICE".

Ændr følgende:

ONLYOFFICE Docs-adresse: Her tilføjes ONLYOFFICE-ip'en.
Hemmelig nøgle: Her tilføjes nøglen.
