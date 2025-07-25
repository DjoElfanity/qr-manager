# 🎯 QR Manager

> **Système de gestion de QR Codes dynamiques avec analytics intégrés**

## ✨ Fonctionnalités

- 🎯 **QR Codes dynamiques** - Changez les URLs sans refaire les QR codes
- 📊 **Analytics intégrés** - Tracking des scans en temps réel
- 🎨 **Interface moderne** - Design responsive avec ShadCN/UI
- ⚡ **Redirection instantanée** - Performance optimisée
- 🏷️ **Système de tags** - Organisation facile des campagnes
- 🔄 **Contrôle total** - Activation/désactivation en un clic
- 📱 **Mobile-first** - Optimisé pour tous les appareils

## 🚀 Aperçu

### 🎮 Démo

- **Dashboard** : Gestion complète des QR codes
- **Génération** : QR codes visuels téléchargeables
- **Redirection** : `/r/ABC123` → destination finale
- **Analytics** : Statistiques de scans détaillées

## 🛠️ Stack Technique

### Frontend

- **Framework** : Next.js 15 (App Router)
- **Language** : TypeScript
- **Styling** : TailwindCSS v4 + ShadCN/UI
- **State** : TanStack Query v5
- **Forms** : React Hook Form + Zod validation

### Backend & Data

- **Storage** : localStorage (demo) / PostgreSQL (production)
- **ORM** : Prisma (configuré)
- **Auth** : BetterAuth (préparé)

### Outils & Dev

- **QR Generation** : qrcode.js
- **Dates** : date-fns
- **Icons** : Lucide React
- **Notifications** : Sonner

## 📦 Installation

### Prérequis

- Node.js 18+
- npm/yarn/pnpm

### Installation rapide

```bash
# Cloner le repository
git clone https://github.com/votre-username/qr-manager.git
cd qr-manager

# Installer les dépendances
npm install

# Lancer en développement
npm run dev
```

L'application sera disponible sur [http://localhost:3000](http://localhost:3000)

### Installation complète avec PostgreSQL

```bash
# 1. Copier les variables d'environnement
cp .env.example .env.local


# 3. Lancer les migrations Prisma
npx prisma migrate dev --name init
npx prisma studio # Vérifier la base
```

## 🏗️ Structure du Projet

```
src/
├── app/                    # Next.js App Router
│   ├── (dashboard)/       # Pages protégées
│   ├── r/[shortCode]/     # Redirection des QR codes
│   ├── layout.tsx         # Layout principal
│   └── page.tsx           # Dashboard
├── components/
│   ├── ui/                # Composants ShadCN
│   └── qr-codes/          # Composants métier
│       ├── QRCodeTable.tsx
│       ├── CreateQRCodeDialog.tsx
│       └── QRCodeDisplay.tsx
├── hooks/
│   └── useQRCodes.ts      # Hooks React Query
├── lib/
│   ├── storage.ts         # Service localStorage
│   └── utils.ts           # Utilitaires
└── types/
    └── qr.ts              # Types TypeScript
```

## 🎯 Utilisation

### Créer un QR Code

1. **Cliquez** sur "Nouveau QR Code"
2. **Remplissez** le nom et l'URL de destination
3. **Ajoutez** des tags (optionnel)
4. **Générez** et téléchargez le QR code

### Gérer les QR Codes

- **✅ Activer/Désactiver** : Contrôle instantané
- **📊 Voir les stats** : Nombre de scans
- **📝 Modifier** : Changer l'URL sans refaire le QR
- **🗑️ Supprimer** : Avec confirmation

### URLs de redirection

Format : `https://votre-domaine.com/r/ABC123`

Chaque QR code génère une URL courte unique qui :

- **Track** automatiquement les scans
- **Redirige** instantanément vers la destination
- **Reste fonctionnelle** même si vous changez l'URL

## 📊 Analytics

Le système track automatiquement :

- **Nombre total** de scans
- **Date et heure** de chaque scan
- **User Agent** (type d'appareil)
- **Referrer** (source du scan)

## 🚀 Déploiement

### Vercel (recommandé)

```bash
# Installation Vercel CLI
npm install -g vercel

# Déploiement
vercel
```

### Autres plateformes

```bash
# Build de production
npm run build

# Export statique (si besoin)
npm run export
```

## 🔧 Configuration

### Variables d'environnement

```bash
# .env.local
DATABASE_URL="postgresql://..."
NEXTAUTH_SECRET="your-secret"
NEXTAUTH_URL="http://localhost:3000"
```

### Customisation

- **Couleurs** : Modifiez `tailwind.config.js`
- **Domaine** : Changez l'URL dans `lib/storage.ts`
- **Analytics** : Intégrez Google Analytics si besoin

## 🤝 Contribution

Les contributions sont les bienvenues !

### Workflow Git

```bash
# Nouvelle fonctionnalité
git checkout -b feature/nouvelle-fonctionnalite
git commit -m "feat: ajouter nouvelle fonctionnalité"
git push origin feature/nouvelle-fonctionnalite
```

### Types de commits

- `feat:` Nouvelle fonctionnalité
- `fix:` Correction de bug
- `docs:` Documentation
- `style:` Formatting, styling
- `refactor:` Refactoring
- `test:` Tests

## 🐛 Issues Connues

- **localStorage** : Fonctionne en mode demo, migrer vers PostgreSQL pour la production
- **QR Codes** : Générés côté client, considérer un service dédié pour de gros volumes

## 📋 Roadmap

### v2.0 - Fonctionnalités avancées

- [ ] Authentification utilisateurs
- [ ] Dashboard analytics avancé
- [ ] API REST complète
- [ ] Export des données
- [ ] Thèmes personnalisables

### v3.0 - Enterprise

- [ ] Multi-tenancy
- [ ] Intégrations tierces
- [ ] API webhooks
- [ ] Géolocalisation
- [ ] A/B Testing intégré

## 📄 Licence

MIT © [Votre Nom](https://github.com/votre-username)

## 🙏 Remerciements

- [Next.js](https://nextjs.org/) pour le framework
- [ShadCN/UI](https://ui.shadcn.com/) pour les composants
- [Vercel](https://vercel.com/) pour l'hébergement
- [Lucide](https://lucide.dev/) pour les icônes

---

⭐ **Si ce projet vous aide, n'hésitez pas à lui donner une étoile !**
#   q r - m a n a g e r  
 