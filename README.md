# SOBAC Mobile SDK — Application Commerciaux

> Reconstruction de l'application mobile Resco SOBAC avec **Salesforce Mobile SDK** et **React Native TypeScript**.

---

## 🎯 Objectif

Remplacer fonctionnellement l'application Resco Mobile utilisée par les commerciaux SOBAC, sans copier le code source propriétaire de Resco. Les fonctionnalités sont reconstruites à partir des règles métier, des métadonnées Salesforce et des retours utilisateurs.

---

## 🏗️ Architecture

| Couche | Technologie |
|---|---|
| Mobile | React Native + TypeScript |
| Accès Salesforce | Salesforce Mobile SDK |
| Authentification | OAuth 2.0 via Connected App Salesforce |
| Synchronisation (v2) | SmartStore + Mobile Sync (à venir) |
| Métadonnées Salesforce | Salesforce DX (SFDX) |

---

## 📁 Structure du projet

```
SOBAC-MOBILESSDK-DEV/
├── src/
│   ├── api/           # Couche d'accès données Salesforce (isolée)
│   ├── components/    # Composants React Native réutilisables
│   ├── screens/       # Écrans de l'application
│   ├── navigation/    # Navigation (React Navigation)
│   ├── hooks/         # Hooks personnalisés
│   ├── store/         # État global (Redux / Context)
│   ├── types/         # Types TypeScript métier
│   └── utils/         # Utilitaires
├── sfdx/              # Métadonnées Salesforce DX
├── docs/              # Documentation fonctionnelle et technique
├── __tests__/         # Tests unitaires et d'intégration
└── android/ ios/      # Code natif généré par React Native
```

---

## 🔐 Sécurité

- **Aucun secret, token ou mot de passe** ne doit être commité dans ce dépôt.
- Respecter les règles CRUD, la sécurité des champs et le partage Salesforce.
- Toute fusion ou déploiement doit faire l'objet d'une **Pull Request validée** par un humain.
- Seule la **sandbox Salesforce autorisée** est utilisée en développement.

---

## 🌿 Convention Git

| Branche | Usage |
|---|---|
| `main` | Code stable, validé — **ne jamais modifier directement** |
| `develop` | Branche d'intégration |
| `feature/<nom>` | Développement d'une fonctionnalité |
| `fix/<nom>` | Correction de bug |
| `release/<version>` | Préparation d'une release |

---

## 🚀 Mise en route (développeur)

```bash
# Cloner le dépôt
git clone https://github.com/gmaniaval/SOBAC-MOBILESSDK-DEV.git
cd SOBAC-MOBILESSDK-DEV

# Installer les dépendances
npm install

# iOS uniquement
cd ios && pod install && cd ..

# Lancer sur Android
npx react-native run-android

# Lancer sur iOS
npx react-native run-ios
```

> ⚠️ Voir `docs/SETUP.md` pour la configuration complète (Connected App Salesforce, variables d'environnement, etc.)

---

## 📋 Statut du projet

- [x] Initialisation du dépôt
- [ ] Configuration React Native + Salesforce Mobile SDK
- [ ] Authentification OAuth Salesforce
- [ ] Module Comptes (Accounts)
- [ ] Module Contacts
- [ ] Module Opportunités
- [ ] Module Activités / Rapports de visite
- [ ] Tests unitaires
- [ ] Build de recette (sandbox)

---

## 👥 Équipe

| Rôle | Personne |
|---|---|
| Chef de projet | Fabien VIDAL |
| Développeur principal | gmaniaval |

---

*Projet confidentiel SOBAC — Ne pas distribuer.*
