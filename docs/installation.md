# Installation & démarrage

> **Rien à installer sur ton ordi** avec Codespaces. Sinon, une version locale est décrite plus bas.

## Option A — GitHub Codespaces (recommandé, tout dans le navigateur)

1. **Use this template** → **Create a new repository** (tu obtiens ta propre copie du projet).
2. Sur ton repo : bouton **`< > Code`** → onglet **Codespaces** → **Create codespace on main**.
3. Patiente ~2 min : VS Code s'ouvre dans le navigateur, l'environnement s'installe **tout seul** (Node 20, dépendances, base de données) grâce au `.devcontainer`.
4. Lance l'app : dans le terminal intégré (**☰ → Terminal → New Terminal**), tape :
   ```
   npm run dev
   ```
5. Une bulle **Open in Browser** apparaît (ou onglet **PORTS** → port **3000**) → l'app s'affiche.

### Si ça coince
- **Erreur de version Node ?** Le Codespace n'a pas pris le `.devcontainer` → supprime-le et recrée-en un.
- **Port 3000 ne s'ouvre pas ?** Onglet **PORTS** → clic droit sur 3000 → **Open in Browser**.
- **Console d'install longue ?** Attends la fin de la première installation, puis relance `npm run dev`.

### Gérer ses Codespaces
- Reprendre / supprimer : **github.com/codespaces**. Un Codespace inactif se met en veille (ne consomme pas le quota gratuit ~60h/mois).

## Option B — En local

Prérequis : **Node 20+**.
```bash
npm install
printf 'DATABASE_URL="file:./dev.db"\n' > .env
npx prisma migrate deploy
npx prisma generate
npx tsx prisma/seed.ts
npm run dev            # http://localhost:3000
```

## Vérifier que tout marche
```bash
npx vitest run         # doit afficher les tests verts
```
