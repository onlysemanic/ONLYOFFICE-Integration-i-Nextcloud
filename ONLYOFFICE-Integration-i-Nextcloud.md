# Installationsguide til at integrere ONLYOFFICE i Nextcloud

Følg denne guide for at integrere ONLYOFFICE i Nextcloud

---

## 1. Åben ONLYOFFICE-konfigurationsfilen

```bash
sudo nano /etc/onlyoffice/documentserver/local.json
```

---

## 2. Tilføj en hemmelig nøgle til JWT-konfigurationen

```bash
      "secret": {
        "browser": {
          "string": "<nøgle>"
        },
        "inbox": {
          "string": "<nøgle>"
        },
        "outbox": {
          "string": "<nøgle>"
        },
        "session": {
          "string": "<nøgle>"
        }
      }
```

---

## 3. Genstart ONLYOFFICE-tjenesterne

```bash
sudo systemctl restart ds-docservice 
sudo systemctl restart ds-converter
```

---

## 4. Kontrollér om ONLYOFFICE-tjenesterne kører

```bash
sudo systemctl status ds-*
```

---

## 5. Installér ONLYOFFICE-appen i Nextcloud

1. Åben Nextcloud i din foretrukne webbrowser.
2. Vælg "Apps" eller "Udvalgte Apps".
3. Find ONLYOFFICE.
4. Download og aktivér appen.

---

## 6. Konfigurér ONLYOFFICE i Nextcloud

1. Gå til "Systemindstillinger".
2. Vælg "ONLYOFFICE" i menuen.
3. Indtast følgende oplysninger:
ONLYOFFICE Docs-adresse: IP'en til ONLYOFFICE.
Hemmelig nøgle: Det er nøglen, som blev indsat i local.json.

---

ONLYOFFICE er nu integreret i Nextcloud.
