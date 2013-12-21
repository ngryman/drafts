## Contexte

### Nombre de devices et Internet

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
- avant le cross platform signifiait cross OS, cross hardware.
- maintenant cela signifie egalement cross screen, cross input.

## Qui ça intéresse?

- Potentiellement tout le monde qui cree des applications!
  - Marche tres vaste.
  - "Inepuisable"
- Qui?
  - Studio de developpements (LVL-like) (qui concoivent)
    - E-commerce
    - Vitrines
    - Gouvernements
    - Applications
  - Saas (qui vendent)
    - Social networks: Facebook
    - Services: Shopify, Soundcloud, Medium
  - Particuliers (qui communiquent)
    - Blogs: Tumblr, Wordpress, perso
    - Portfolios: 500px

## Solutions existantes

### HTML5

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

### Responsive design

- Adaptif → Responsive
  - sites mobiles / desktop → mêmes sites.
- Maintenabilité : Le meme code pour tous les ecrans.
- Layout flexible.
- Adapte au changement.
- Communication: Une URL.

## Pas si vite... les images ?

- 60% du poids d'une page sont des images, et c'est en augmentation [[3]]
- En 3 ans, le poids des pages a plus que doublé. [[2]]
- Depuis l'an dernier, le poids moyen d'une page est passé de 1MB a 1.5MB [[4]]
- 500 M+ de photos uploadees par jour [[1]]
  - croissance exponentielle
- Répartition:
  - 50% sont des JPEG, donc photos.
  - 25% sont des GIF, ui et internet memes.
  - 25% sont des PNG, ui.
- Graphique de la composition des images de 3 projets LVL: HNIC, AMC

[1]: http://fr.slideshare.net/kleinerperkins/kpcb-internet-trends-2013
[2]: http://httparchive.org/compare.php
[3]: http://httparchive.org/interesting.php#bytesperpage
[4]: http://mobile.smashingmagazine.com/2013/10/24/automate-your-responsive-images-with-mobify-js

http://royal.pingdom.com/2011/11/21/web-pages-getting-bloated-here-is-why/

## Problématique

==> Service les **mêmes images** sur **tous les devices**, **partout** et de manière **performante**.

- graphique : ligne droite des resolutions, approximation avec des rectangle
  - on peut considerer la droite comme une infinite de resolutions.
  - comme upscaling est mauvais, approximation par le haut.
  - aire entre la droite et le rectangle represente la perte.
  
### Ce que le RWD ne resout pas...

- Ne répond que partiellement à la problèmatique.
  - picture et srcset.
- Implique une gestion des images côté dev.
- graphique : ligne droite des resolutions, approximation avec des rectangle
  - on peut considerer la droite comme une infinite de resolutions.
  - comme upscaling est mauvais, approximation par le haut.
  - aire entre la droite et le rectangle represente la perte.
- On va se fixer un idéal : images flexibles.

## Solutions actuelles

On va séparer des facteurs cles du success en deux:
  - Entrepise, total sur 10
  - Utilisateur, total sur 10
Pour simplifier, moyenne d'une note qui peut dépendre selon l'implémentation / application et autres.

### Aucune

- Aucun traitement particulier
- Entrepsie
   - Installation: 5/5 - Rien
   - Temps: 5/5 - Rien
   - Changement: 5/5 - Rien
   - Maintenance: 5/5 - Rien
   - Scalability: 5/5 - Rien
   - Prix: 3/5 - Frais de bande passante, processing serveur
- Utilisateur
  - Qualite: 4/5 - La plus haute résolution possible, donc bon (on va voir que ça dépend des navigateurs)
  - Attente: 0/5 - le pire scénario
  - Fluidité: 2/5 - dépend de l'application
- TOTAL:
  - Entreprise: 4.5/5 (28/30)
  - Utilisateur: 2/5 (0-6/15)
  - **3/5** (6.5/10)
  - TODO: add note en fonction des profils
- Visuel courbe (adaptif)
- Commentaire: solution la plus avantageuse pour l'entreprise.

### Manuelle

- Resize dans Photoshop ou autres
- Entreprise:
  - Installation: 4/5 - En général seulement un logiciel, souvent déjà présent
  - Temps: 0/5 - Chronophage
  - Changement: 0/5 - Pas dutout adapté au changement
  - Maintenance: 5/5 - Rien à maintenir
  - Scalability: 0/5 - Terrible
  - Prix: 4/5 - éventuelles licences logicielles
- Utilisateur
  - Qualite: 4/5 - Dépend de comment c'est fait
    - En général mal (de mon expèrience)
      - Resizing fait de manière naive: perte de qulité des images
      - Souvent ré-encodage de l'image: ouverture -> resize -> sauvegarde.
      - Double resizing (source + navigateur) -> dégradation forte de la qualité
  - Attente: 3/5 - Dégradation gracieuse implique une perte plus on s'éloigne du breakpoint
    - Breakpoint en général fait de manière intelligente, donc moins de monde s'éloigne.
  - Fluidité: 4/5 - Pas toujours pixel perfect
- TOTAL:
  - Entreprise: 2/5 (13/30)
  - Utilisateur: 3.5/5 (11/15)
  - **2.5/5** (5.5/10)
  - TODO: add note en fonction des profils
- Visuel courbe (adaptif)

### Asset pipeline (phase de build)

- Via grunt ou autres
- Avantages: automatisé
- Installation: 1/5 - en general compose d'une tool chain qu'il faut configurer, déployer, etc...
- Temps: 3/5 - Une fois en place, le temps de resizing est presque négligeable. Cependant:
  - Selon le nombre d'images et la taille du projet peu prendre du temps machine.
- Changement: 4/5 - En général pas trop compliqué d'ajouter de nouveaux formats.
- Maintenance: 3/5 - Dépend encore une fois de la tool chain / projet. Peu poser problème lors de changements d'environnements, ...
- Scalability: 4/5 - Bon
- Prix: 4/5 - en général solutions open source, on perd tout de meme de la bande passante
- Utilisateur
  - Qualite: 3/5 - Dépend de la configuration des outils, moins bon que l'oeil humain
  - Attente: 4/5 - Plus car outils qui optimisent les images sont communs.
  - Fluidité: 4/5 - Même que la précédente.
- TOTAL:
  - Entreprise: 3/5 (19/30)
  - Utilisateur: 3.5/5 (11/15)
  - **3/5** (6.5/10)
  - TODO: add note en fonction des profils
- Visuel courbe (adaptif)

### On Demand

- Via solutions open sources
- Installation: 1/5 - aussi chiant que l'asset pipeline.
- Temps: 5/5 - Automatisé, on demand only.
- Changement: 3/5 - Changer les configuration, tester.
- Maintenance: 3/5 - Dépend de la configuration / serveur / projet. Peu poser problème lors de changements d'environnements, ...
- Scalability: 4/5 - Bon
- Prix: 5/5 - en général solutions open source
- Utilisateur
  - Qualite: 3/5 - Dépend de comment c'est fait, offrir le meilleur resizing, constant pour tous les navigateurs (en générale optimisé pour la performance). Les navigateurs emploient differents types de resizing qui font que le resultat peut varier. De plus ils sont plus dans l'optique de choisir des algos performants que qualitatifs.
  - Attente: 4/5 - Optimale, mais dépend de comment le cache et CDN sont configuré
  - Fluidité: 5/5 - Pixel perfect.
- TOTAL:
  - Entreprise: 3.5/5 (21/30)
  - Utilisateur: 4/5 (12/15)
  - **3.5/5** (7.5/10)
  - TODO: add note en fonction des profils
- Visuel courbe (adaptif)
- Visuel courbe (parfaite/fluide)

### Peut-on arriver a 5/5 ?

Oui !

## RIBS

**Rideau? Arrivee des device avec l'image de RIBS, puis le logo qui fait apparaitre les mots Responsive Images Backed Server-side**.
**Son?**

- RIBS: Responsive Images Backed Server-side
- RESS
  - Responsive Design + Server Side Components
  - Un sereur peut stocker, caculer et envoyer.
  - Il peut egalement mutualiser: faire l'opération une fois pour tous.
- Esprit
  - Performance
  - Qualité
  - Scalability
  - Rendre le Web meilleur B]

### Pitch

- SaaS + CDN
- Hautes performances
- Prix faible

### SaaS + CDN

- Service de processing d'image, payable à l'image.
  - On paye se qu'on consomme
  - Pas de barrières, de BFR
- CDN
  - On paye encore moins car Cloudflare -> gratuit
  - Rapide
  - Géo-localisé
- Détection client
- Console de gestion
  
### Hautes performances

- Stack Node.js & natif (C++)
- Gestion des quotas, mémoire, SIMD

### Futures possibilites

- Pre-caching
- Permettre de modifier les parametres de sharpening (et autres) par image.
- Détection cliente a d'autres plateformes: iOS, Android, Wordpress, etc...
- Partenariats avec des plateformes de blogging ou autres.

### Voyons-voir...

- Oui, solution sur le cloud: SaaS: Software as a Service
- Installation: 5/5 - Pratiquement rien.
- Temps: 5/5 - Rien.
- Changement: 5/5 - Parfait.
- Maintenance: 5/5 - Parfait.
- Scalability: 5/5 - Parfait.
- Prix: 5/5 - Meilleur compromis.
- Utilisateur
  - Qualite: 5/5 - Le meilleur possible.
  - Attente: 5/5 - Le meilleur possible.
  - Fluidité: 5/5 - Le meilleur possible.
- TOTAL:
  - Entreprise: 5/5 (30/30)
  - Utilisateur: 5/5 (15/15)
  - **5/5** (10/10)
  - TODO: add note en fonction des profils
- Visuel courbe (adaptif)
- Visuel courbe (parfaite/fluide)

- A CE POINT, ON A PRESENTE QU'ON CHOISIT LA MEILLEURE SOLUTION POSSIBLE QUI REPOND LE MIEUX AUX CLIENTS POTENTIELS. IL NE RESTE PLUS QU'A DEMONTRER NOTRE AVENTAGE CONCURRENTIEL.

### Concurrents

- TODO: note en fonction des profils
- responsive.io
- ress.io
- adaptive-images.com
- resrc.it
   - liste
   - etat des lieux
   - comparaison
   - cdn intelligents: akamai

### Avantages concurrentiels

- Prix
  - prix adaptifs et degressifs
- Performances
- Qualité
- Scaling

- A CE POINT, ON A CONVAINCU QUE NOTRE PRODUIT EST LE MEILLEUR.

- EXPLIQUER LE CONTEXTE, QUE LES CONCURRENTS ET LA PRESSE ONT DEJA COMMUNIQUE SUR LE SUJET. IL NE RESTE PLUS QU'A NOUS FAIRE CONNAITRE.

## Comment se faire connaitre ?

- Presse specialisee
- Beta avec cles beta
- Reseaux sociaux
- Vecteurs du Web
- Conferences ?
- Kickstarter

## Projections financieres / Modèle économique

### Économie d'échelle

- CM = CT / q
  - avec CT = 14.4 + 20 = **34.4**
            = 40.3 + 20 = **60.3**

## Merci

### Oh ! Attendez j'ai oublié quelque chose ...

- Use the source Luke. (avec Yoda from Impress.js).

## Open Source (effet vitesse lumière sur le slide)

## Qu'est-ce que c'est ?

- Important dans le Web, qui est full open source, qui a un plus fort esprit OS que n'importe quel autre domaine.
  - les gens sont habitués à la gratuité•
- LVL et l'open source (logos pour les projets qu'on utilise)
  - Toolchain, IDE, serveurs: majorite open source
  - Purple: full open source, node.js, mongodb, AngularJS
  - Bell: node.js, AngularJS, jQuery, grunt, Phonegap, LESS
  - AMC: node.js, jQuery, Lodash, Compass
- On utilise l'open-source comme **outil qu'on utilise** ou **fondation qu'on leverage** (exemple de Mac OS: BSD, Chrome/Safari: Chromium).

## En 2013

- Ne plus voir l'open source comme dans les annees 2000, c'est aussi...
- Une communaute enorme (Github seulement: 3.5M utilisateurs mi 2013), a suivi la tendance Web 2.0
  - Web 2.0 = contenu créé par les gens
- Comme dans toute communauté il y a:
  - des leaders (stars)
  - des modes
- Communaute de Nodejs [[1]]
  - Grande, plus grande croissance
    - python:  29,720 packages / 22 years = 1351 packages per year
    - ruby:    54,385 packages / 18 years = 3022 packages per year
    - node.js: 26,966 packages / 4 years  = 6742 packages per year
    - nuget:   17,513 packages / 3 years  = 5837 packages per year
      - http://en.wikipedia.org/wiki/NuGet
      - http://www.nuget.org/
  - JavaScript #1 sur Github [[2]]
    - 264131 repos en 6 mois (janvier - aout)

- good summary: https://groups.google.com/forum/#!topic/nodejs/BiZGuJsNjMM
[1]: http://caines.ca/blog/programming/the-node-js-community-is-quietly-changing-the-face-of-open-source/
[2]: http://adambard.com/blog/top-github-languages-for-2013-so-far/

## Ribs est né dans l'open source

- https://github.com/h5bp/server-configs-node/issues/13 (10 months)
- Devait faire partie intégrante de H5BP node-server
- h5b: organisation la plus connues dans le milieu du Web, et de tout Github:
  1. twitter bootstrap (62k)
  2. jquery (27k)
  3. node (26k)
  4. h5bp (23k)
- Paul Irish: Google Chrome, Modernizr, Yeoman, jQuery
  - Github: 9.4k
  - Twitter: 99 342
- Chris Coyer: css tricks, codepen
  - Github: 2.4k
  - Twitter: 94 442
- Addy Osmani: Google Chrome, Yeoman, TodoMVC, Grunt, Bower, jQuery
  - Github: 5.8k
  - Twitter: 49 806
- Mathias Bynens: whatwg, lodash
  - Github: 1.4k
  - Twitter: 15 7666
- Sindre Sorhus: Yeoman, Grunt, Bower
  - Github: 1.5k
  - Twitter: 8 978
- Nicolas Gallagher: Twitter, Bower
  - Github: 2.2k
  - Twitter: 17 000
- Divya Manian: Adobe, topcoat
  - Github: 837
  - Twitter: 16 287
- Lea Verou: W3C
  - Github: 3.3k
  - Twitter: 39 988

## Nouveaux avantages

### Communication

- Marketing
  - http://www.journaldunet.com/solutions/expert/43840/le-marketing--faiblesse-ou-force-de-l-open-source.shtml
  - Attirer les dev
    - D'abord les comprendre (ça tombe bien j'en suis un)
    - API sexy, etc...
    - seduire les developpeurs directement, et non les entreprises: se sont eux qui font les choix technologiques
    - Exemple de Mozilla qui a pris des parts de marchés considérables a Internet Explorer.
    - Exemple de Chrome avec Google (dérivé en Chrome Book, Chrome Store)
      - Stratégie lente de conquête du Web
      - Presque tous les devs utilisent Chrome maintenant
      - Si demain Google sort un produit payant relatif a Chrome, tout le monde achète.
  - Apache
  - MySQL
  - ...
  - Imager.js, 4e de la trend Github en decembre 2013:
    - https://github.com/trending?l=javascript&since=monthly
    - https://github.com/BBC-News/Imager.js
- Notoriété : l'image !
- Fidélisation
  - C'est du community management, a grande echelle, par le code.

### Produit

- Extensible
- Stable, qualité supérieure
  - Trouver des exemple de comparaison OS vs proprio:
    - Chrome (Chromium) vs Internet Explorer
    - Joyent vs Azure
  - Le propriétaire est bridé, il peut marquer des points à son arrivée, mais sera vite dépassé par la vague de projet OS. On ne peut pas lutter contre des M de devs qui collaborent entre eux.
  - Le modèle propriétaire devient même moins adapté dans certains secteurs : le Web en est l'exemple parfait.
- Colle le plus à la demande
  - En contact direct avec les utilisateurs qui sont pro-actifs
  - Possibilité de mettre en place des bounties:
    - Etablir une top list de features.
    - Permettre de prioriser des items dans cette liste via des bounties.

### Stratégique

- Diversification
  - Fork et specialisation dans d'autres domaines, auquels on aurait peut-etre pas pensé.
- Freemium gratuit pour nous:
  - Solution open-source correspond exactement au modèle, sans cout pour nous
- Adoption par de grosses structures
- Pénétration à presque 100% dans le marché potentiel

## Risques potentiels

- Propriété intellectuelle
  - Licences ! Ce n'est pas le far west.
- Concurrence
  - Nous sommes les maitres de notre technologie, au yeux de TOUS grace a l'Open Source.
  - Pas si simple de s'approprier une technologie
  - Nous aurons toujours un chapitre d'avance
- Perte de clients potentiels
  - N'auraient probablement pas été des clients
  - Vecteurs de communication
  - Potentiels utilisateurs plus tard ! (moi avec Github / Spotify par ex) - comparable au Freemium mais sans coûts !!

## Stratégies, à choisir (besoin de leur aide)

- Dual-licensing
  - Empeche la concurrence
  - Bride l'OS, l'image.
- Closed-source puis open-source
  - Minimise les risques early
  - Moins exposé
  - Crowd Funding, bounty sur Kickstarter pour:
    - fixer les bugs, développer de nouvelle features.
    - Release le projet open source, tirer profit d'etre le seul projet potentiellement open source.
      - On peut voir ca comme une sorte de don dans le milieu.
- Baseline + Advanced versions
  - Pour moi la meilleure balance

http://oss-watch.ac.uk/resources/duallicence2
  
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

- Etat actuel des images
  - images adaptives **au mieux**.
  - mauvaise utilisation du cache [[1]]
  - resize souvent manuel, ou automatique, faible qualité
  - mauvais choix de compression pour JPEG
  - pas d'adaptation aux nouveaux formats émergeants (WebP).

[1]: http://httparchive.org/interesting.php#caching

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