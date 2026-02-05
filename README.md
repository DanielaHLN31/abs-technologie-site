# 🚀 Site Web ABS Technologie Group

Site web statique moderne et professionnel pour **ABS TECHNOLOGIE Group SARL** - Distributeur agréé Samsung et représentant exclusif Orange au Bénin.

## ✨ Caractéristiques

### Design & UX
- 🎨 Design moderne avec palette de couleurs sophistiquée (bleu technologie + orange)
- ⚡ Animations fluides et interactions micro
- 📱 Responsive design (mobile, tablette, desktop)
- 🎭 Typographie distinctive (Playfair Display + Montserrat)
- 🌊 Effets de parallax et scroll animations

### Fonctionnalités
- 📧 Formulaire de contact intégré avec Netlify Forms
- 🔢 Compteurs animés pour les statistiques
- 🎯 Navigation smooth scroll
- 💫 Cartes flottantes avec effets 3D
- 📊 Section services avec 4 offres principales
- 🤝 Showcase des partenaires (Samsung & Orange)
- 📞 Informations de contact complètes

### Performance & SEO
- ⚡ Site 100% statique (HTML/CSS/JS pur)
- 🚀 Chargement ultra-rapide
- 🔍 Optimisé pour le SEO
- 📱 Meta tags pour réseaux sociaux
- 🔒 Headers de sécurité configurés

## 📁 Structure du Projet

```
abs-technologie/
├── index.html          # Page principale
├── styles.css          # Styles CSS
├── script.js           # JavaScript
├── netlify.toml        # Configuration Netlify
└── README.md           # Documentation
```

## 🚀 Déploiement sur Netlify

### Option 1 : Déploiement via interface web Netlify

1. **Créer un compte Netlify** : [netlify.com](https://netlify.com)
2. **Importer le site** :
   - Cliquez sur "Add new site" → "Deploy manually"
   - Glissez-déposez tous les fichiers du projet
3. **Configuration automatique** : Netlify détecte le `netlify.toml`
4. **Votre site est en ligne** ! 🎉

### Option 2 : Déploiement via Git

1. Créez un repository Git (GitHub, GitLab, Bitbucket)
2. Poussez les fichiers :
   ```bash
   git init
   git add .
   git commit -m "Initial commit - ABS Technologie website"
   git remote add origin <votre-repo-url>
   git push -u origin main
   ```
3. Sur Netlify : "Add new site" → "Import from Git"
4. Connectez votre repository
5. Netlify déploie automatiquement à chaque commit !

### Option 3 : Netlify CLI

```bash
# Installer Netlify CLI
npm install -g netlify-cli

# Se connecter
netlify login

# Déployer
netlify deploy --prod
```

## 🎨 Personnalisation

### Couleurs

Modifiez les variables CSS dans `styles.css` :

```css
:root {
    --primary-blue: #0066CC;      /* Bleu principal */
    --orange-accent: #FF6600;     /* Orange accent */
    --dark: #0A0E1A;              /* Texte sombre */
}
```

### Contenu

1. **Informations de contact** : Remplacez dans `index.html` :
   - Adresse complète
   - Numéros de téléphone
   - Email

2. **Services** : Modifiez les 4 cartes de services selon vos offres

3. **Textes** : Personnalisez tous les textes selon votre identité

### Formulaire de Contact

Le formulaire utilise **Netlify Forms**. Après le déploiement :

1. Allez dans Netlify Dashboard → Forms
2. Vous recevrez les soumissions par email
3. Configuration des notifications : Settings → Forms → Form notifications

### Ajouter Google Analytics

Ajoutez avant `</head>` dans `index.html` :

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

### Ajouter Facebook Pixel

Ajoutez après `<head>` dans `index.html` :

```html
<!-- Facebook Pixel -->
<script>
  !function(f,b,e,v,n,t,s)
  {if(f.fbq)return;n=f.fbq=function(){n.callMethod?
  n.callMethod.apply(n,arguments):n.queue.push(arguments)};
  if(!f._fbq)f._fbq=n;n.push=n;n.loaded=!0;n.version='2.0';
  n.queue=[];t=b.createElement(e);t.async=!0;
  t.src=v;s=b.getElementsByTagName(e)[0];
  s.parentNode.insertBefore(t,s)}(window, document,'script',
  'https://connect.facebook.net/en_US/fbevents.js');
  fbq('init', 'YOUR_PIXEL_ID');
  fbq('track', 'PageView');
</script>
```

## 🔧 Optimisations Avancées

### Ajouter des images

1. Créez un dossier `images/`
2. Ajoutez vos images optimisées (WebP recommandé)
3. Référencez-les dans le HTML

### Lazy Loading

Les images peuvent être chargées de manière différée :

```html
<img data-src="images/photo.jpg" alt="Description" class="lazy">
```

### PWA (Progressive Web App)

Ajoutez un `manifest.json` :

```json
{
  "name": "ABS Technologie Group",
  "short_name": "ABS Tech",
  "description": "Distributeur Samsung & Orange au Bénin",
  "start_url": "/",
  "display": "standalone",
  "background_color": "#0066CC",
  "theme_color": "#0066CC",
  "icons": [
    {
      "src": "/icon-192.png",
      "sizes": "192x192",
      "type": "image/png"
    }
  ]
}
```

## 📱 Réseaux Sociaux

Liens à configurer dans le footer :

- **Facebook** : `https://facebook.com/abstechnologiegroup`
- **WhatsApp** : Remplacez le `#` par votre lien WhatsApp Business

## 🆘 Support & Maintenance

### Tester en local

Ouvrez simplement `index.html` dans votre navigateur, ou utilisez :

```bash
# Avec Python
python -m http.server 8000

# Avec Node.js
npx http-server

# Avec PHP
php -S localhost:8000
```

### Résolution de problèmes

- **Formulaire ne fonctionne pas** : Vérifiez que vous avez déployé sur Netlify
- **Animations lentes** : Réduisez les `transition-duration` dans le CSS
- **Responsive cassé** : Testez avec les DevTools du navigateur

## 📈 Prochaines Étapes

1. ✅ Déployer sur Netlify
2. 📸 Ajouter des photos de produits Samsung/Orange
3. 🎥 Intégrer des vidéos de démonstration
4. 📝 Créer un blog avec Netlify CMS (optionnel)
5. 🛒 Ajouter un catalogue de produits
6. 💬 Intégrer un chat en direct (Tawk.to, Crisp)

## 📄 Licence

Ce projet a été créé spécifiquement pour **ABS TECHNOLOGIE Group SARL**.

## 🤝 Contact

Pour toute question sur le site :
- **Email** : contact@abstechnologie.com
- **Téléphone** : +229 01 96 06 26 26
- **Adresse** : Cotonou, Bénin

---

**Développé avec 💙 pour ABS Technologie Group**

Distributeur agréé Samsung | Représentant exclusif Orange au Bénin
