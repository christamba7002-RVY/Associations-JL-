# AJL – Association Jeunesse et Leadership
### Site web officiel · République Démocratique du Congo

![AJL Banner](public/favicon.svg)

Un site web moderne, responsive et professionnel pour la gestion complète d'une association — membres, cotisations, dons, subventions et communication.

---

## 🚀 Fonctionnalités

| Module | Fonctionnalités |
|--------|----------------|
| **Accueil** | Présentation, statistiques animées, appel à l'action |
| **Inscription membres** | Formulaire multi-étapes, génération automatique de matricule |
| **Cotisations** | Paiements MTN, Airtel, carte bancaire, PayPal |
| **Dons** | Locaux (mobile money) et internationaux (PayPal, Stripe) |
| **Subventions** | Vérification d'éligibilité, formulaire de dossier, code unique |
| **Actualités** | Grille d'articles dynamique |
| **Contact** | Formulaire de contact avec notifications |

---

## 📁 Structure du projet

```
ajl-website/
├── index.html              # Page principale (site complet)
├── public/
│   └── favicon.svg         # Icône de l'association
├── src/
│   ├── styles/
│   │   └── main.css        # Design system complet
│   └── utils/
│       └── main.js         # Logique interactive
└── README.md
```

---

## 🛠️ Installation & Démarrage

### Option 1 — Ouvrir directement
Double-cliquez sur `index.html` dans votre navigateur. Aucun serveur requis.

### Option 2 — Serveur local (recommandé)
```bash
# Avec Python
python -m http.server 8000

# Avec Node.js (npx)
npx serve .

# Avec VS Code → Extension "Live Server"
```
Ouvrez ensuite : `http://localhost:8000`

---

## 🌐 Déploiement

### GitHub Pages (gratuit)
1. Pushez ce repo sur GitHub
2. Allez dans **Settings → Pages**
3. Source : `main` branch, dossier `/root`
4. Votre site sera en ligne sur `https://votre-username.github.io/ajl-website`

### Netlify (gratuit, recommandé)
1. Connectez votre repo GitHub à [netlify.com](https://netlify.com)
2. Build command : *(laisser vide)*
3. Publish directory : `.`
4. Deploy automatique à chaque push !

### Hostinger / OVH / cPanel
Uploadez tous les fichiers via FTP dans le dossier `public_html/`.

---

## 🔧 Personnalisation

### Changer le nom de l'association
Dans `index.html`, remplacez :
- `AJL` → votre sigle
- `Association Jeunesse et Leadership` → votre nom complet
- `ajl-asso.org` → votre domaine

### Changer les couleurs
Dans `src/styles/main.css`, modifiez les variables CSS :
```css
:root {
  --green:       #1a6b3c;  /* Couleur principale */
  --green-light: #27a85e;  /* Couleur secondaire */
  --gold:        #c9a227;  /* Couleur accent */
  --dark:        #0d1f14;  /* Fond sombre */
}
```

### Modifier les montants des cotisations
Dans `index.html`, section `#cotisations` :
```html
<div class="pay-amount">5 000 <span>FC/mois</span></div>
<div class="pay-amount">50 000 <span>FC/an</span></div>
```

### Ajouter de vraies actualités
Dans `src/utils/main.js`, modifiez le tableau `newsData` :
```js
const newsData = [
  {
    emoji: '🌱',
    tag: 'Programme',
    title: 'Titre de votre actualité',
    text: 'Description de l\'actualité...',
    date: '15 Déc 2024',
  },
  // ...
];
```

---

## 📱 Modes de paiement intégrés

| Méthode | Type | Statut |
|---------|------|--------|
| MTN Mobile Money Congo | Local | ✅ Instructions affichées |
| Airtel Money Congo | Local | ✅ Instructions affichées |
| PayPal | International | ✅ Instructions affichées |
| Carte bancaire | International | ✅ Instructions affichées |
| Stripe | International | ✅ Instructions affichées |

> **Note :** Les paiements réels nécessitent l'intégration d'une API backend (Node.js/Laravel) et des clés API des fournisseurs de paiement.

---

## 🔒 Sécurité (Phase 2 — Backend)

Pour la version production complète, il faudra ajouter :
- [ ] Backend API (Node.js + Express ou Laravel)
- [ ] Base de données (PostgreSQL ou MySQL)
- [ ] Authentification JWT + codes 2FA à 6 chiffres
- [ ] Intégration APIs de paiement (MTN MoMo API, Airtel API, Stripe, PayPal)
- [ ] Stockage sécurisé des documents (AWS S3 ou équivalent)
- [ ] Envoi d'emails automatiques (SendGrid ou Mailgun)
- [ ] Panneau d'administration sécurisé

---

## 📋 Feuille de route

### Version 1 (actuelle) — Site statique ✅
- [x] Design complet responsive
- [x] Formulaire d'inscription multi-étapes
- [x] Génération de matricule
- [x] Interface de paiement
- [x] Système de subventions (front-end)
- [x] Actualités
- [x] Contact

### Version 2 — Backend & Paiements
- [ ] API REST (Node.js)
- [ ] Base de données membres
- [ ] Paiements réels MTN/Airtel
- [ ] Emails automatiques

### Version 3 — Fonctionnalités avancées
- [ ] Espace membre connecté
- [ ] Tableau de bord administrateur
- [ ] Système d'observateurs terrain
- [ ] Tirage au sort automatisé
- [ ] Données biométriques

---

## 🤝 Contribution

Les contributions sont les bienvenues ! Forkez le projet et soumettez une Pull Request.

---

## 📄 Licence

Ce projet est sous licence MIT. Libre d'utilisation pour des associations à but non lucratif.

---

*Fait avec ❤️ pour la jeunesse africaine.*
# Associations-JL-
site web de L'AJL 
