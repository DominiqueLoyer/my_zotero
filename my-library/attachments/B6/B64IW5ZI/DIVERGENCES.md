	# ⚠️ DIVERGENCES — Vérification PDF vs BibTeX

Généré le 2026-02-24 12:46 — SysCRED

---

**1 divergence(s) détectée(s)**

| # | Clé BibTeX | Titre attendu | Problème | Action requise |
|---|-----------|--------------|----------|----------------|
| 1 | `Hitzler2025Survey` | Neuro-Symbolic AI Survey 2024-2025 | Titre partiel (2/3 mots), auteur ✗ | 🟡 Vérifier manuellement |

---

## Instructions pour corriger dans LaTeX

Si la **clé BibTeX doit changer** (mauvais auteur/titre/année),
utilisez la commande suivante pour mettre à jour votre `.tex` :

```bash
python3 ~/Scripts/bibtex_batch.py references.bib --fix-tex these.tex
```

Le script demandera les remplacements de clés et mettra à jour
tous les `\citep{}`, `\cite{}`, `\citet{}` automatiquement.

---

## Détail des divergences

### `Hitzler2025Survey`
- **Titre attendu** : Neuro-Symbolic AI Survey 2024-2025
- **Auteur attendu** : Hitzler, Pascal and others
- **Année** : 2025
- **Problème** : Titre partiel (2/3 mots), auteur ✗
- **Type** : ⚠️ Correspondance partielle
