# Mjärdevi Lunch Skill

Hämtar dagens lunchmeny från alla restauranger i Mjärdevi via Luncha I Mjärdevi API.

## Installation

1. Skaffa API-nyckel på https://lunchaimjardevi.com/api/

2. Skapa `.api_key` fil:
```bash
echo "din_api_nyckel" > .api_key
```

3. Kör scriptet:
```bash
python scripts/get_lunch.py
```

## Användning

```bash
# Använd API-nyckel från .api_key fil
python scripts/get_lunch.py

# Ange API-nyckel direkt
python scripts/get_lunch.py din_api_nyckel

# JSON-format
python scripts/get_lunch.py din_api_nyckel json
```

## Filer

- `SKILL.md` - Skill-dokumentation
- `scripts/get_lunch.py` - Huvudscript
- `references/api.md` - API-dokumentation
- `.gitignore` - Exkluderar .api_key
- `.api_key.example` - Mall för API-nyckel
