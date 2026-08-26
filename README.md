# AD STUDIO — Site vitrine (Astro)

Site vitrine one-page pour AD STUDIO, studio photo/podcast et salle de réunion
à Serris (77).

## Démarrer en local

```bash
npm install
npm run dev
```

Le site est servi sur http://localhost:4321

## Build de production

```bash
npm run build
npm run preview
```

Le dossier `dist/` généré est prêt à héberger (Netlify, Vercel, o2switch, etc.).

## Structure

```
src/
  layouts/Layout.astro     -> squelette HTML + SEO
  components/
    Header.astro            -> nav + logo
    Hero.astro               -> accroche + gros titre
    Marquee.astro            -> bandeau défilant signature
    Services.astro           -> les 8 offres, groupées par pôle
    Studio.astro              -> adresse, distances, carte
    Reseaux.astro             -> service réseaux sociaux / contenu
    Contact.astro              -> formulaire de devis
    Footer.astro                -> pied de page
  pages/index.astro          -> assemble toutes les sections
  styles/global.css          -> tokens de couleur, typographies, boutons
public/
  logo.png, logo-blanc.png   -> vos logos fournis
```

## À personnaliser avant la mise en ligne

- `src/components/Contact.astro` : remplacer l'email et le téléphone
  placeholders (`contact@ad-studio-serris.fr`, `+33 (0)0 00 00 00 00`) par vos
  vraies coordonnées, et brancher le formulaire sur un service d'envoi
  (Formspree, Resend, un webhook...) — le `mailto:` actuel est un dépannage
  minimal, pas fiable sur tous les navigateurs/mobiles.
- `src/components/Studio.astro` : la carte utilise des coordonnées
  approximatives pour Serris ; vérifiez le point exact et ajustez si besoin.
- Ajouter vos vraies photos du studio (actuellement le site est 100% typo/couleur,
  vous pouvez glisser des visuels dans `public/` et les appeler dans les
  composants Hero / Studio pour renforcer l'impact).
- Réseaux sociaux : ajouter les liens réels dans le Footer si vous le souhaitez.

## Palette & typographie

- Couleurs : `#FF4474` (rose), `#FF89A9` (rose clair), `#FF7E00` (orange),
  `#231F20` (encre), `#000000`, `#FFFFFF` — définies dans
  `src/styles/global.css` (`:root`).
- Typo : Archivo Black (titres), Inter (texte courant), Space Mono (labels/eyebrows).
