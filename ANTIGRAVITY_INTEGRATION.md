# ANTIGRAVITY — INSTRUCTIONS D'INTÉGRATION
# Pour Claude Code / Antigravity : intégrer pricing_gold_time_v3.html dans le site Gold Time

## CE QUI A CHANGÉ (V3 vs V2):
1. Prix après 6 mois SUPPRIMÉS — remplacés par un agenda qualitatif (3 cartes: E-commerce, WhatsApp bot, Expansion média) SANS chiffres
2. Meilleur design fusionné (le hero de Gemini + le pricing structuré de Cowork)
3. Images Unsplash réelles au lieu des placeholders
4. Scroll reveal animations
5. Shape-shifter images (cycle entre 2 visuels)
6. Sections content preview (FB + TikTok mockups)
7. Budget pub = 900₪ au lieu de 1000₪ (match le brief David)

## FICHIER À INTÉGRER:
`~/Desktop/GOLD_TIME/pricing_gold_time_v3.html`

## COMMENT INTÉGRER DANS LE SITE gold-time-jerusalem.vercel.app:

### Option A: Route /pricing dans le site Express existant
```javascript
// Dans server-local.js, ajouter cette route:
app.get('/pricing', (req, res) => {
    res.sendFile(path.join(__dirname, 'public', 'pricing.html'));
});
// Copier pricing_gold_time_v3.html → public/pricing.html
```

### Option B: Page standalone (plus simple)
Copier le fichier dans le dossier public:
```bash
cp ~/Desktop/GOLD_TIME/pricing_gold_time_v3.html \
   ~/Desktop/_CLIENTS_ACTIFS/GOLD_TIME_DEMO/gold-time-web/public/pricing.html
```
Accessible via: gold-time-jerusalem.vercel.app/pricing.html

### Option C: Déployer séparément (si le site principal n'est pas prêt)
```bash
cd ~/Desktop/GOLD_TIME/
npx serve . -p 3001
# ou deployer sur Vercel comme un site standalone
```

## VIDÉOS À REMPLACER:

Le HTML référence 2 vidéos MP4 dans le hero et la section projections:
1. `Luxury_watch_and_202603191612.mp4` — Hero background
2. `Luxury_watch_mechanism_202603191615.mp4` — Section pricing background

David crée ces vidéos sur Google Flow. Quand elles sont prêtes:
```bash
# Copier les vidéos dans le même dossier que le HTML
cp /path/to/david_video_hero.mp4 public/Luxury_watch_and_202603191612.mp4
cp /path/to/david_video_mechanism.mp4 public/Luxury_watch_mechanism_202603191615.mp4
```

Si les vidéos ne sont pas encore prêtes, le HTML fonctionne quand même (fond noir).

## IMAGES SHAPE-SHIFTER:

Les images dans la section roadmap viennent d'Unsplash (gratuites):
- Image 1: Luxury jewelry display
- Image 2: Luxury watch closeup

Pour remplacer par les vraies photos Gold Time (Nano Banana):
```html
<img src="VOTRE_IMAGE_NANOBANANA_1.jpg" class="active" alt="Gold Time Collection">
<img src="VOTRE_IMAGE_NANOBANANA_2.jpg" alt="Gold Time Watches">
```

## LIEN DANS LE MENU DU SITE:

Ajouter dans la nav du site Gold Time:
```html
<a href="/pricing.html" class="text-gold">הצעה מסחרית</a>
```

## STYLE: IDENTIQUE AU SITE
- Même fonts: Cinzel (serif) + Heebo (sans) + Playfair Display (luxury italic)
- Même couleurs: --gold: #D4AF37, --navy: #050A1A, --dark: #030303
- Même glass-panel effect
- Même Tailwind CDN
- Toggle HE/FR intégré

## DEPLOY:
```bash
cd ~/Desktop/_CLIENTS_ACTIFS/GOLD_TIME_DEMO/gold-time-web/
git add public/pricing.html
git commit -m "add: pricing page for Gold Time proposal"
vercel --prod --token=$VERCEL_TOKEN
```
