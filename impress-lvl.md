## Contexte

### HTML5

- http://www.evolutionoftheweb.com/?hl=fr#/evolution/day
- fin 2010
- La fin du HTML versionne, le debut d'une nouvelle ere
  - cycle de developpement des navigateurs hyper accelere (Firefox: 15 jours, Chrome: 15/30 jours)
  - fin du bridage technologique de IE
  - 3D, canvas, acceleration materielle
  - JavaScript 4e language le plus utilise au monde [[1]]
- cross platform par excellence
- propulse par les mobiles et particulierement l'iPhone.

[1]: http://langpop.com

### Explosion de devices

- 16% du traffic sont des tablettes / mobiles [[1]]
- croissance x8 des mobiles par rapport au desktop [[2]]
- dans les 4 prochaines annees, la croissance est prevue a x26 [[2]]
- android domine 80% du marche [[4]]
  - plus de 300 devices [[3]]
- croissance d'android -> plus grande segmentation -> plus de tailles d'ecrans [[3]]

[1]: http://blogs.adobe.com/digitalmarketing/digital-index/tablets-trump-smartphones-in-global-website-traffic
[2]: http://fr.slideshare.net/livefront/responsive-design-7877412
[3]: http://developer.android.com/about/index.html
[4]: http://appleinsider.com/articles/13/11/12/idc-data-shows-66-of-androids-81-smartphone-share-are-junk-phones-selling-for-215

### Explosions des images

- 500 M+ de photos uploadees par jour [[1]]
  - croissance exponentielle
- 

[1]: http://fr.slideshare.net/kleinerperkins/kpcb-internet-trends-2013

### Responsive design

- Le meme code pour tous les ecrans.
- Layout flexible.

### Performance as design

> It’s time for us to treat performance as an essential design feature, not just as a technical best practice. - Brad Frost

==> Accéder à la **même application** sur **tous les devices**, de **n'importe où** et de manière **performante**.

## Problematique des images

- Etat actuel des images: images adaptives.
- graphique : ligne droite des resolutions, approximation avec des rectangle
  - on peut considerer la droite comme une infinite de resolutions.
  - comme upscaling est mauvais, approximation par le haut.
  - aire entre la droite et le rectangle represente la perte.
- but : image flexibles.

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