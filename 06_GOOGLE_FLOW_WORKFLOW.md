# GOOGLE FLOW — WORKFLOW CRÉATION VIDÉO GOLD TIME
# Instructions pas à pas pour David dans Google Flow (labs.google/flow)

---

## ACCÈS:
1. Ouvre: https://labs.google/flow
2. Connecte-toi avec: dreamnovaultimate@gmail.com
3. Clique "Create New"

---

## VIDÉO FLOW #1 — HERO LANDING PAGE (16:9, 15-20s)

### Prompt Google Flow:
```
Create a luxury cinematic video for a high-end jewelry store in Jerusalem called Gold Time.

The video should show:
- Opening: Warm golden light on ancient Jerusalem stone walls
- Transition: Camera moves toward an elegant jewelry store window
- Main shot: Sparkling diamond jewelry and luxury Swiss watches displayed in pristine glass cases
- Close-up: A gold watch face reflecting light, creating bokeh effects
- Closing: Store interior with warm ambient lighting

Style: Ultra-premium, think Cartier or Bulgari commercial
Color: Golden warm tones, deep blacks, high contrast
Music: Elegant piano with subtle strings
Duration: 15-20 seconds
Ratio: 16:9 (widescreen)
```

### Instructions:
1. Colle le prompt dans Google Flow
2. Sélectionne "Video" comme output
3. Choisis 16:9
4. Génère et attends (~2-3 min)
5. Télécharge en MP4
6. Sauvegarde: goldtime_flow_hero.mp4

---

## VIDÉO FLOW #2 — TIKTOK VERTICAL (9:16, 10-15s)

### Prompt Google Flow:
```
Create a vertical TikTok-style luxury jewelry video:

Quick cuts, trendy music feel:
- Shot 1 (0-3s): Slow-motion hand opening a luxury gift box, gold ribbon
- Shot 2 (3-7s): Close-up of diamond bracelet catching light, sparkle effects
- Shot 3 (7-10s): Gold watch on a wrist against Jerusalem stone background
- Shot 4 (10-15s): Store interior beauty shot, warm lighting

Style: TikTok luxury trend aesthetic, fast cuts, satisfying visuals
Color: Rich golds, deep blacks, warm highlights
NO TEXT OVERLAY (we add text in editing)
Duration: 10-15 seconds
Ratio: 9:16 (vertical)
```

---

## VIDÉO FLOW #3 — PESSAH AMBIANCE (1:1, 15s, pour Facebook)

### Prompt Google Flow:
```
Create a Passover celebration luxury video:

Scene: An elegant Seder table setting — white tablecloth, silver cups, candles burning softly.
Camera slowly reveals a luxury jewelry gift box in the center of the table.
A woman's hand with a gold bracelet opens the box — inside, a stunning diamond pendant necklace.
Warm candlelight, intimate family atmosphere, premium feel.

Closing: Soft fade to black with golden shimmer effect.

Style: Emotional, intimate, premium gift-giving moment
Color: Warm candle tones, gold accents, soft whites
Duration: 15 seconds
Ratio: 1:1 (square for Facebook)
```

---

## SI DAVID A DES PHOTOS RÉELLES À INTÉGRER:

### Workflow avec photo existante:
1. Upload la photo dans Google Flow
2. Prompt: "Transform this still photo of a jewelry store into a cinematic slow-motion video. Add subtle camera movement (parallax effect), light animation (sparkling diamonds), and atmosphere (golden bokeh). Keep the original photo recognizable. 10 seconds, same aspect ratio."
3. Génère et télécharge

### Workflow avec photo de la vitrine King George:
1. David prend la photo sur place
2. Upload dans Flow
3. Prompt: "Create a 10-second cinematic video from this jewelry store photo. Add: slow push-in camera movement, sparkling light effects on the jewelry in the window, warm golden color grade, ambient luxury feel. The store should look like it belongs in a Cartier commercial."

---

## EXPORT & INTÉGRATION:

### Pour la landing page HTML:
Remplace le placeholder vidéo dans le hero:
```html
<video class="hero-video" autoplay muted loop playsinline>
    <source src="goldtime_flow_hero.mp4" type="video/mp4">
</video>
```

### Pour TikTok:
Upload directement le MP4 vertical (9:16)

### Pour Facebook:
Upload le MP4 carré (1:1) avec le texte du copywriting (fichier 04_COPYWRITING_SOCIAL.md)
