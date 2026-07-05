# Starter — Liste d'agents (Decode 4A)

Point de départ du TP : **Next.js + TypeScript + Prisma (SQLite) + Vitest**, prêt à l'emploi.

## Démarrer (GitHub Codespaces — recommandé)
1. Clique **Use this template** → **Create a new repository** (tu obtiens ta propre copie).
2. Sur ton nouveau repo : **`< > Code` → onglet Codespaces → Create codespace on main**.
3. Attends ~2 min (installation automatique via `.devcontainer`).
4. Dans le terminal : `npm run dev` → ouvre le port **3000**.

## Ce qui est déjà fait
- Scaffold **Next.js** (App Router) + TypeScript
- **Prisma + SQLite** : modèle `Agent`, migration, seed → base prête
- **Vitest** configuré pour le TDD
- `.devcontainer` : **Node 20** + setup auto (Codespace opérationnel du premier coup)

## Ce que tu construis (via les prompts du cours)
- La couche **domaine** (`lib/domain/agent.ts`) + ses **tests TDD**
- La **page** qui liste les agents depuis la base
- Une **feature** au choix, en TDD
- Le **déploiement** (Vercel + Neon), puis un **mini-pentest** OWASP

---
*En local (sans Codespaces) : `npm install` → crée un `.env` avec `DATABASE_URL="file:./dev.db"` → `npx prisma migrate deploy && npx prisma generate` → `npx tsx prisma/seed.ts` → `npm run dev`.*
