# Ressources accessibilité

## Sites web

| Ressource                                                                                                                                                                                  | Description                                                              |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------ |
| [validator.w3.org](https://validator.w3.org/)                                                                                                                                              | Permet de vérifier que la structure HTML respecte les conventions        |
| [lighthouse](https://chromewebstore.google.com/detail/lighthouse/blipmdconlkpinefehnmjammfjpmpbjk)                                                                                         | Outil de diagnostique d'un site web présent sur les navigateurs chromium |
| [devtools-guide-chromium](https://learn.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium/accessibility/reference)                                                                | Liste des outils de chrome à utiliser pour vérifier l'accessibilité      |
| [windows accessibility shortcuts](https://support.microsoft.com/en-us/windows/windows-keyboard-shortcuts-for-accessibility-021bcb62-45c8-e4ef-1e4f-41b8c1fc87fd#WindowsVersion=Windows_10) | Liste des raccourcis à utiliser sur Windows pour l'accessibilité         |
| [design.numerique.gouv](https://design.numerique.gouv.fr/)                                                                                                                                 | Parle d'accessibilité, mémo dev et designer                              |
| [patterns-aria](https://www.w3.org/WAI/ARIA/apg/patterns/)                                                                                                                                 | Liste d'exemples de patterns ARIA accessible                             |
| [react-aria-live](https://www.npmjs.com/package/react-aria-live)                                                                                                                           | library react pour faciliter l'utilisation de l'attribut `aria-live`     |
| [a11yproject](https://www.a11yproject.com/)                                                                                                                                                | Nombreuses références sur l'accessibilité et une checklist complète !    |
| [inclusive-components](https://book.inclusive-components.design/)                                                                                                                          | Livre sur la réalisation de composants accessibles                       |
| [criteres-et-tests-rgaa](https://accessibilite.numerique.gouv.fr/methode/criteres-et-tests/)                                                                                               | L'ensemble des critères testés sur le RGAA                               |

## CSS

- [practical-ui](https://www.practical-ui.com/)
- [1linelayouts](https://1linelayouts.glitch.me/)
- [moderncss](https://moderncss.dev/)
- [cube](https://cube.fyi/)
- [buildexcellentwebsit.es](https://buildexcellentwebsit.es/)

## Réalisation d'un audit

### Analyse automatisée

1. Lancer une analyse Lighthouse depuis les devtools d'un navigateur Chromium
2. Utiliser les DevTools de Edge
   1. Consulter l'onglet `Problèmes`
   2. Aller dans l'onglet `Aperçu CSS` et lancer une analyse
   3. Inspecter différents éléments HTML de la page avec le sélecteur d'éléments `CTRL + SHIFT + C`
3. Dans l'onglet `Rendu` émuler les déficiences visuelles et vérifier les contrastes de couleurs
4. Utiliser les extensions et outils suivantes selon le besoin :
   - [Validator W3C](https://validator.w3.org/)
   - [Colour Contrast Analyser](https://www.tpgi.com/color-contrast-checker/)
   - [WCAG Color Contrast Checker](https://chromewebstore.google.com/detail/wcag-color-contrast-check/plnahcmalebffmaghcpcmpaciebdhgdf?hl=en)
   - [Headings Map](https://chromewebstore.google.com/detail/headingsmap/flbjommegcjonpdmenkdiocclhjacmbi?hl=en)
   - [Wave Evaluation DevTools](https://chromewebstore.google.com/detail/wave-evaluation-tool/jbbplnpkjmmeebjpijfedlgcdilocofh?hl=en)
   - [Accessibility Insight for Web](https://accessibilityinsights.io/)

### Analyse manuelle

1. Vérifier les contrastes des textes sur les gradients et les images
2. Vérifier que les textes alternatifs correspondent bien à l'image
3. Les balises ARIA sont définies sur les bons éléments et au bon endroit
4. Vérifier le focus au clavier : ordre logique, pas de focus sur un élément invisible de la page
5. Vérifier les iFrame : présence d'un titre, focus visible au clavier
6. Vérifier les vidéos présentes le site : sous-titres ou transcription si possible

### Analyse avec assistance technologique

Utilisation des outils comme [NVDA](https://www.nvda.fr/), VoiceOver, [JAWS](https://www.ceciaa.com/jaws-logiciel-revue-ecran.html), ou le narrateur.

| Element              | NVDA (Windows)      | VoiceOver (macOS)        |
| -------------------- | ------------------- | ------------------------ |
| General command keys | Insert              | Control+Option           |
| Stop audio           | Control             | Control                  |
| Read next/prev       | ↓ or ↑              | Control+Option+→ or ←    |
| Start reading        | Insert↓             | Control+Option+A         |
| Element List/Rotor   | NVDA + F7           | Control+Option+U         |
| Landmarks            | D                   | Control+Option+U         |
| Headings             | H                   | Control+Option+Command+H |
| Links                | K                   | Control+Option+Command+L |
| Form controls        | F                   | Control+Option+Command+J |
| Tables               | T                   | Control+OptionCommand+T  |
| Within Tables        | InsertAlt + ↓ ↑ ← → | Control+Option+↓ ↑ ← →   |
