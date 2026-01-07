# Crypto Loop – GitHub Pages Deployment

Dieses Projekt ist eine statische Seite (reines HTML/JS/CSS) und kann direkt über GitHub Pages veröffentlicht werden.

## Deployment (GitHub Pages mit Actions)

- Quelle: GitHub Actions (Workflow ist bereits enthalten unter .github/workflows/pages.yml)
- Branch: `main`
- Output: Projektwurzel (dieser Ordner)

### Schritte

1. Neues Repository auf GitHub erstellen (oder dieses lokal verbundene Repo verwenden).
2. Dateien pushen:

```bash
# im Projektordner
git init
git add .
git commit -m "Initial commit: GitHub Pages setup"
git branch -M main
git remote add origin https://github.com/<USER>/<REPO>.git
git push -u origin main
```

3. In den Repository-Einstellungen auf GitHub:
   - Settings → Pages → Build and deployment → Source: „GitHub Actions“ auswählen.
   - Der bereitgestellte Workflow „Deploy to GitHub Pages“ baut und veröffentlicht automatisch bei jedem Push nach `main`.