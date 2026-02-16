# Installation och Setup

## 1. Skaffa API-nyckel

Registrera en gratis API-nyckel på:
https://lunchaimjardevi.com/api/

## 2. Konfigurera API-nyckel

Skapa en `.api_key` fil i skill-rotkatalogen:

```bash
echo "din_api_nyckel_här" > .api_key
```

Eller kopiera exempel-filen:
```bash
cp .api_key.example .api_key
# Redigera sedan .api_key med din faktiska nyckel
```

**OBS:** `.api_key` är inkluderad i `.gitignore` och kommer aldrig committas till git.

## 3. Kör scriptet

```bash
# Använd API-nyckel från .api_key fil
python scripts/get_lunch.py

# Eller ange API-nyckel direkt (överskrider .api_key fil)
python scripts/get_lunch.py din_api_nyckel_här

# Få JSON-output
python scripts/get_lunch.py din_api_nyckel_här json
```

## Filstruktur

```
mjardevi-lunch/
├── SKILL.md              # Huvud skill-dokumentation
├── SETUP.md              # Denna fil
├── .gitignore            # Gitignore (exkluderar .api_key)
├── .api_key.example      # Mall för API-nyckel
├── .api_key              # Din API-nyckel (gitignored)
├── scripts/
│   ├── get_lunch.py      # Huvudscript
│   └── .api_key.example  # Alternativ plats för API-nyckel
└── references/
    └── api.md            # API-dokumentation
```

## Säkerhet

- API-nyckeln lagras lokalt i `.api_key`
- Filen är inkluderad i `.gitignore`
- Dela aldrig din API-nyckel publikt
- Skapa en ny nyckel om den läckt
