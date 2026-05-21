# ONLYOFFICE-Integration i Nextcloud-guide

Følg denne vejledning for at integrere ONLYOFFICE i Nextcloud

---

## 1. Tilgå local.json-filen

```bash
sudo nano /etc/onlyoffice/documentserver/local.json
```

---

## 2. Generer en hemmelig nøgle til secret.browser.string og sæt nøglen ind

```bash
      "secret": {
        "browser": {
          "string": "<nøgle>"
```

---

## 3. Genstart ds-converter og ds-docservice

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

Tilgå Nextcloud og download ONLYOFFICE i Apps. Gå ind på Nextcloud og ændr følgende indstillinger:

ONLYOFFICE Docs-adresse: Her tilføjer man ONLYOFFICE-ip'en.
Hemmelig nøgle: "<nøgle>"
