## Contexte

### HTML5: la 3eme bulle Internet

- http://www.evolutionoftheweb.com/?hl=fr#/evolution/day
- fin 2010
- La fin du HTML versionne, le debut d'une nouvelle ere pour les technologies Web
  - cycle de developpement des navigateurs hyper accelere (Firefox: 15 jours, Chrome: 15/30 jours)
  - fin du bridage technologique de IE
  - 3D, canvas, acceleration materielle
  - JavaScript 4e language le plus utilise au monde [[1]]
- cross platform par excellence
- propulse par les mobiles et particulierement l'iPhone.

[1]: http://langpop.com

### # de devices et Internet

- 16% du traffic sont des tablettes / mobiles [[1]]
- Dans certains pays, le mobile est la seule maniere d'accéder à Internet.
- croissance x8 des mobiles par rapport au desktop [[2]]
- dans les 4 prochaines annees, la croissance est prevue a x26 [[2]]
- android domine 80% du marche [[4]]
  - plus de 300 devices [[3]]
- croissance d'android -> plus grande segmentation -> plus de tailles d'ecrans [[3]]

[1]: http://blogs.adobe.com/digitalmarketing/digital-index/tablets-trump-smartphones-in-global-website-traffic
[2]: http://fr.slideshare.net/livefront/responsive-design-7877412
[3]: http://developer.android.com/about/index.html
[4]: http://appleinsider.com/articles/13/11/12/idc-data-shows-66-of-androids-81-smartphone-share-are-junk-phones-selling-for-215

### Performance as design

> It’s time for us to treat performance as an essential design feature, not just as a technical best practice. - Brad Frost

- Histoire du mec qui a optimise son site et qui a vu ses performances chutter
  - apres investigation il s'est rendu compte que le nombre de visiteurs des pays en vois de developpement avait explose car son site ne prenait plus que quelques secondes a charger sur leur reseau, au lieu de plus d'une minute.

- Dans un secteur ultra concurrentiel, la performance permet egalement de se demarquer.
- Impacte les entreprises: image perfmatters
  - utilisateurs sur mobiles sont impatients
- Impacte les utilisateurs
  - meilleure experience
  - reseau (3G)
  - batterie
- Pour l'utilisateur, la performance se résume:
  - au temps d'attente après chaque action (chargement initial, changement de page, changements UI).
  - a la fluidité visuelle de la UI.

http://www.globaldots.com/how-website-speed-affects-conversion-rates/
http://www.globaldots.com/10-reasons-to-speed-up-your-website/

## Problematique

==> Accéder à la **même application** sur **tous les devices**, **partout** et de manière **performante**.

### Une solution (partielle): responsive design

- Adaptif → Responsive
  - sites mobiles / desktop → mêmes sites.
- Le meme code pour tous les ecrans.
- Layout flexible.
- Ne répond que partiellement à la problèmatique.
  - picture et srcset.

### Explosions des images

- En 3 ans, le poids des pages a plus que doublé. [[2]]
- Depuis l'an dernier, le poids moyen d'une page est passé de 1MB a 1.5MB [[4]]
- 60% du poids d'une page sont des images, et c'est augmentation [[3]]
- 500 M+ de photos uploadees par jour [[1]]
  - croissance exponentielle
- Répartition:
  - 50% sont des JPEG, donc photos.
  - 25% sont des GIF, ui et internet memes.
  - 25% sont des PNG, ui.

[1]: http://fr.slideshare.net/kleinerperkins/kpcb-internet-trends-2013
[2]: http://httparchive.org/compare.php
[3]: http://httparchive.org/interesting.php#bytesperpage
[4]: http://mobile.smashingmagazine.com/2013/10/24/automate-your-responsive-images-with-mobify-js

http://royal.pingdom.com/2011/11/21/web-pages-getting-bloated-here-is-why/

### Problematique des images

Reprend la problematique initiale: Servir des images sur **tous les devices**, **partout** et de manière **performante**.

### Solutions existantes

- Etat actuel des images
  - images adaptives **au mieux**.
  - mauvaise utilisation du cache [[1]]
  - resize souvent manuel, ou automatique, faible qualité
  - mauvais choix de compression pour JPEG
  - pas d'adaptation aux nouveaux formats émergeants (WebP).
  
### Reponse partielle du responsive design

- graphique : ligne droite des resolutions, approximation avec des rectangle
  - on peut considerer la droite comme une infinite de resolutions.
  - comme upscaling est mauvais, approximation par le haut.
  - aire entre la droite et le rectangle represente la perte.
- but : image flexibles.

[1]: http://httparchive.org/interesting.php#caching

- Objectifs
  - Performance
  - Qualité
  - Scalability
  
- Solution
  - Calcul du cout par image moyen
  - Nombre de declinaisons d'une image moyen
  - Prix a la consommation
  - Exemple de l'evolution d'un site et de sa consommation aupres de notre service
  - Comparatif avec les concurrents
  - Obstacles:
    - renvoie un image cheap
    - cout de marketing
  - Performance c'est sexy pour les dev. C'est un peu une quete technique.
    - Une solution performante va attirer, intriguer (surtout si elle se compare a l'existant).
    
- Profil developpeur, a developper trolololo

- Planning
  - Service + com
  - reglage de la beta (les devs open source ne pourront de toutes facons pas nous aider car le projet est trop early stage).
  - Feedback bugs, features.
  - Bounty sur Kickstarter pour:
    - bugs, features.
    - Release le projet open source, tirer profit d'etre le seul projet potentiellement open source.
      - On peut voir ca comme une sorte de don dans le milieu.
  - En cas d'echec, ce n'est pas grave
    - On devrait commencer a generer des revenus et utilisateurs qui valident la viabilite du projet
    - On peut egalement en parallele aller chercher des investisements plus classiques

- Open source rejoute un gap: passer du gratuit au payant.
  - Payant est tellement faible que le ratio gain de temps / prix est tres interessant.
  - 