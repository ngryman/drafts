- Web = technologie != de site Internet
* - SaaS = Software as a Service
- seduire les developpeurs directement, et non les entreprises
  - se sont eux qui font les choix technologiques
- offrir le meilleur resizing, constant pour tous les navigateurs:
  - eviter de laisser le navigateur resizer permet aussi d'avoir le controle sur la qualite de l'image resizee. Les navigateurs emploient differents types de resizing qui font que le resultat peut varier. De plus ils sont plus dans l'optique de choisir des algos performants que qualitatifs.
- permettre de modifier les parametres de sharpening (et autres) par image.
  - generer un hash unique a partir de la data + parametres.
  
- s'associer a des plateformes de blogging ou autres.

## contexte (quoi?)

 - explosion HTML5, revirement des entreprises pour cette technologie (TODO: fresque)
   - bcp de monde utilise et de plus en plus
   - cross platform
 - explosion du nombre de devices et de l'heterogeneite (TODO: chiffres: gros chiffre visuel)
     - montrer la croissance et la domination
   - diversite des reseaux
   - plus de 50% du traffic web mobile
 - course vers la performance
   - google sanctionne les site non performants
   - performance 0.1 second = x% de rebond
 
## problematique
   
 - acceder au meme site / app a partir de n'importe quel device, de n'importe ou, de maniere performante
 - responsive design comme solution partielle qui repond uniquement a "acceder sur n'importe quel device"
   - ne repond pas a "n'importe ou, et de maniere performante"
   - doit etre utilisee en parallele de best practices et autres outils pour atteindre ces objectifs.
   - en expliquant, le responsive repond partiellement a la gestion des images
 - le plus grosse problematique est la gestion des images
   - 70% du contenu sont des images (TODO: comparaison de la structure des sites, courbe)
     - analyse de 3 projets de LVL

## problematique des images

 - explications
   - images: photos, ui
 - toujours confronte a cette problematique dans toutes mes experiences pro
 - exemple playtouch: jeux video HTML5 sur mobile
   - plusieurs tailles de jeux fixes
   - pipeline d'asset couteuse
 - meme problematique a LVL
 
## besoins (pourquoi?)

 - solutionner cette problematique
   - concurrentiel, se demarquer: course a la performance
   - explosion des acces Internet dans les pays en voie de developpement ou Internet est uniquement accessible sur mobile
   - pourquoi c'est interessant d'optimiser
 - la presse se charge de sensibiliser les devs/studios, donc burst d'utilisation bientot
   - besoin qui va se developper de plus en plus dans l'avenir
 
## demande (qui?)

 - differents profils (ciblage), 3/4 personnages "techniques"
   - projets existants avec une volonte de repondre a ce probleme
   - nouveux projets
 - application sans serveurs dedies
 - Studios de developmments
 - Sites prives: e-commerce, entreprises, gouvernement, presse, tv, etc...
 - Services en ligne
 - Developpeurs
 
## solutions existantes
 
 - TODO: tableau
 - TODO: referencer a quel profil ca convient
 - aucun, resize navigateur
 - a la main (avantage, inconveniant)
   - demande du temps
   - en general bacle (pas de sharpening, etc...)
     - voir carrément double encodage: ouverture, resizing, sauvarde.
   - pas scalable
   - pas adapte au changement
 - phase de build (avantage, inconveniant)
   - grunt
   - ...
 - resizing/cropping d'image a la volee (avantage, inconveniants: qui seront plus tard invalides par ribs)
   - caching des images
   - standard qui emerge RESS: http://mobile.smashingmagazine.com/2013/10/08/responsive-website-design-with-ress/
   - services sur le cloud
   
   - dans les 2 premiers cas: DOUBLE RESIZING (source + navigateur) -> dégradation forte de la qualité de l'image.
     - une qualité de resizing divergeante selon le navigateur.
 
## idee
 
 - qu'est-ce qu'on veut faire: repondre a la majorite des solutions pour tout le monde
 - explications rapide (pitch)
 
## outil (j'ai pense a)

 - RIBS! : combler les inconvenients existants
   - technologiquement cool
   - focaliser sur la qualite des transformations
   - performance
   - simple d'utilisation
  
## concurrents directs & reponse partielle

- concurrents open source majoritairement
  - concurrents, qualite pas forcement presente
- recoupe les profils et leur eventuelle utilisation

## service

 - platforme sur le cloud, en quoi ca repond mieux
   - facile a utilser
   - instantane
 
## concurrents

 - responsive.io
 - resrc.it
   - liste
   - etat des lieux
   - comparaison
   - cdn intelligents: akamai
 
## avantages concurrentiels
 
  - prix
    - prix adaptifs et degressifs
  - qualite
  - scaling

## modele economique

## plan d'action

 - technique
 - communication
 - ...
 
MAIS ON POURRAIT FAIRE ENCORE MIEUX!
## open source

 - presentation

 - html5boilerplate: explique que ce sont des gurus
   - cette problematique ressort
   - declinaison de html5 boilerplate nodejs
   - pourquoi cette idee
 
 - notoriete technique
 - penetration chez les non-clients
   - qui se convertiront peut etre plus tard a une solution payante
 - publicite via les developpeurs
 - pas de concurrence directe
 - github / twitter: viral (ex: de retweet)
 - communaute
   - proche des besoins utilisateurs
   - q&a gratuite
   - features gratuites
 - nodejs
   - plus grosse communaute en croissance exponentielle
   - performances
   - en contact avec Joyent
 - dangers
   - propriete intellectuelle: licences
   - pas de solution payante: vendre du service
   - 
 - freins
   - configuration

 - lvl sera connue techniquement, prepare l'arrivee de nouveau produits (pas forcement entierement open source)

 - communautre nodejs
   - la plus active au niveau de l'open source
   - en pleine explosion
   - pas d'existant
  - dependances de plusieurs projets open sources
  - bounties
  - debouches
  
## Outil detaille

  - 3 briques assemblees pour offrir un outil complet et extensible
  - couvre tous les fronts (solutions)
 - 3 couches qui repondent chacune a des besoins differents, mais qui se completent pour offrir une solution finale
 - axe de communication enorme
   - API sexy
   - extensibilite

### manipulation d'images

 - resizing, cropping, transcoding, art direction
   - plus performant que l'existant
   - extensible a souhait

### serveur d'images

 - plus performant que l'existant
   - 

### detection client

  - javascript
  - objective-c
  - android
  - autres?
   
## esprit

 - qualite
 - performance
 - facilite d'utilisation
 - state of the art
 - rendre le Web meilleur
 
## FCS

 - prix
 - extensible
 - communaute
 - communication
 
## Couts

 - moi
 - Joyent Standard 2: $38/mo
 - cloudflare por: $20/mo
 - total: $6150/mo
 - 6mo: $36900
   
## avantages concurrentiels

 - open source!
 - prix adaptifs et degressifs
 
## futur

 - art direction
 - art direction dynamique
   
## swot

## modele economique

 - SaaS
 - marque blanche
 - consulting
 
 
 
 
 
## technologies

 - nodejs: evented i/o, javascript
 - C++: manipulation
   - custom IO
   - Leptonica (Google dev) puis custom operations
 - pipeline
 - hooks
 - constraints
 - unit tested
 
## resizing

 - Resampling avec Lanczos 3 kernel
   - renforce les edges (evite de faire un bicubic + unsharp).
   - optimise via la "periode de sampling"
   - possibilite de parallelise (SIMD)
 - optimizations
   - custom allocator: work area = image area + stack area
     - image area: block allocator
     - stack area: obstack

## but (conclusion)

 - state of the art image server
 - consulting
 - optimization
 - small to big compagnies
 - penetrer sur plusieurs fronts

## optimisations

 - pre-caching on idle
 - simd
 - custom allocators

## architecture

 - landing page + site commercial sur Github
 - app sur Joyent
 - cache sur Cloudflare

## exemple open source

 - nodejs / joyent
 - mysql

## communication

 - entonnoir inverse (cf. Mailchimp)
   - pas de 1% de transformation
   - 1% de communication ciblee
 - twitter
 - github
 - beta fermee
 - presse specialisee
 - html5 boilerplate (one of the biggest repo on Github), jquery & node (26k), h5bp (23k)
   - nodejs server maintainer
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
     
- http://tinyletter.com/ben/letters/why-i-hate-funnels
 
## planning

 - 6 mois
 - (details)
 
## besoins

 - fulltime
 - 1 ui/ux pour le site et l'interface d'admin

## recap

 - faibles risques
 - possibilite de diversification enorme

## questions?

## sources

 - http://ress.io
 - https://responsive.io
 - http://www.resrc.it
 - http://adaptive-images.com
 - http://www.sencha.com/learn/how-to-use-src-sencha-io
 - http://mobile.smashingmagazine.com/2013/10/24/automate-your-responsive-images-with-mobify-js/
 - https://developers.google.com/speed/articles/web-metrics
