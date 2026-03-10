Oui, tu peux t’en servir comme “cahier de travail” ici : tu colles ton code, tes snippets, tes notes, et on prépare les changements sans toucher à ce qui fonctionne déjà.

Deux façons efficaces de travailler ici :

Mode “notes” (recommandé pour toi)
Tu mets tout dans NOTES.md, puis quand tu es certain, tu copies seulement les lignes finales dans index.html.

Mode “patch”
Tu me donnes un bloc précis (ex: ton body { ... }), et je te renvoie uniquement le même bloc avec l’ajout minimal.

Quand tu veux, envoie :

soit le bloc body { ... } de ton CSS,
soit ton objectif exact (ex: “wallpaper + rien d’autre, mobile safe”), et je te renvoie la version finale prête à coller.


### Préparation image (recommandations)
- Format conseillé : **WEBP**
- Poids cible : **≤ 600 Ko** (idéal 300–600 Ko)
- Largeur : **1600 à 2000 px** (souvent suffisant pour fond)


@media (min-width: 992px){body{ background-attachment: fixed; }
}

Deux détails pratiques :

Ça marche seulement si ton body a déjà un background-image (sinon ça ne fait rien).
Sur mobile (< 992px), ça restera en mode normal (souvent plus stable).
Si tu veux être encore plus “propre”, tu peux aussi définir explicitement la valeur mobile dans body :
snippet.css 
v2
body{ background-attachment: scroll; }

@media (min-width: 992px){
  body{ background-attachment: fixed; }
}



# NOTES — Clef de Sol (Fusion — La Résilience)

## Objectif
Garder un suivi des améliorations sans modifier le fonctionnement actuel du site (accessibilité déjà testée).

---

## À faire plus tard — Wallpaper (page d’accueil uniquement)
**Principe :** ajouter uniquement du CSS dans `index.html` (dans le bloc `<style>`), sans toucher au reste.

### Snippet minimal (mobile-safe)
À ajouter dans `body { ... }` :

```css
background-image: url("assets/wallpaper.webp");
background-size: cover;
background-position: center;
background-repeat: no-repeat;


# NOTES — Clef de Sol (Fusion — La Résilience)

## Objectif
Garder un suivi des améliorations sans modifier le fonctionnement actuel du site (accessibilité déjà testée).

---

## À faire plus tard — Wallpaper (page d’accueil uniquement)
**Principe :** ajouter uniquement du CSS dans `index.html` (dans le bloc `<style>`), sans toucher au reste.

### Snippet minimal (mobile-safe)
À ajouter dans `body { ... }` :

```css
background-image: url("assets/wallpaper.webp");
background-size: cover;
background-position: center;
background-repeat: no-repeat;
```

### Option PC seulement (évite les bugs mobile)
À ajouter à la fin du `<style>` :

```css
@media (min-width: 992px){
  body{ background-attachment: fixed; }
}
```

### Préparation image (recommandations)
- Format conseillé : **WEBP**
- Poids cible : **≤ 600 Ko** (idéal 300–600 Ko)
- Largeur : **1600 à 2000 px** (souvent suffisant pour fond)

---

## Notes accessibilité
- Ne pas modifier la structure/texte/bouton PDF tant que les tests (ex: Le TAPE Mtl/Laval) restent la référence.
