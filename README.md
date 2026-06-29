# FWF-Schlagwort-Tombola

A tiny static GitHub Pages site that randomly selects an FWF Wissensgebietszweig / Schlagwort from a CSV file and links the result to the FWF Forschungsradar.

## Files

- `index.html` – the full single-page app.
- `schlagwoerter.csv` – category data.

## CSV format

```csv
code,label,path
100000,Naturwissenschaften,Naturwissenschaften
600000,Geisteswissenschaften; Kunstwissenschaften,Geisteswissenschaften; Kunstwissenschaften
```

For subcategories, use `>` in the `path` column:

```csv
code,label,path
601000,Geschichte,Geisteswissenschaften; Kunstwissenschaften>Geschichte
```

The page loads every valid row and randomly draws from those rows only. This is useful because the six-digit system has gaps and not every numeric combination is a real category.

## GitHub Pages

1. Put `index.html`, `schlagwoerter.csv`, and this `README.md` in your repository root.
2. Commit and push.
3. In GitHub, go to **Settings → Pages**.
4. Choose **Deploy from a branch** and select your default branch, root folder `/`.
5. Open the GitHub Pages URL.

## Adjusting categories

Edit only `schlagwoerter.csv`. No JavaScript changes are needed.
