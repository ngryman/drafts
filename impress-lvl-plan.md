- Web = technologie != de site Internet

## contexte

 - explosion HTML5, revirement des entreprises pour cette technologie (TODO: fresque)
   - bcp de monde utilise et de plus en plus
   - cross platform
 - explosion du nombre de devices et de l'heterogeneite (TODO: chiffres: gros chiffre visuel)
     - montrer la croissance et la domination
   - diversite des reseaux
   - plus de 50% du traffic web mobile
 - performance
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

 - toujours confronte a cette problematique dans toutes mes experiences pro
 - c'est venu dans playtouch: jeux video HTML5 sur mobile
   - plusieurs tailles de jeux fixes
   - pipeline d'asset couteuse
 - meme problematique a LVL
 - images: photos, ui
 
## solutions
 
 - phase de build
 - resizing/cropping d'image a la volee
 - caching des images
 - la presse se charge de sensibiliser les devs, donc burst bientot
 - standard qui emerge RESS
 
## idee
 
 - html5boilerplate: explique que ce sont des gurus
   - cette problematique ressort
   - declinaison de html5 boilerplate nodejs
 - pourquoi cette idee

## existant
 
## demande

## besoins

 - application sans serveurs dedies
 - cloud services existants

## open source

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
 
## produit

 - RIBS!
 - 3 couches
 - manipulation d'images
   - resizing, cropping, transcoding, art direction
   - plus performant que l'existant
   - extensible a souhait
 - serveur d'images
   - plus performant que l'existant
   - 
 - detection client
   - javascript
   - objective-c
   - android
   - autres?
   
## esprit

 - qualite
 - performance
 - state of the art

## but

 - state of the art image server
 - consulting
 - optimization
 - small to big compagnies
 - penetrer sur plusieurs fronts

## clients

 - Studios de developmments
 - Sites prives: e-commerce, entreprises, gouvernement, presse, tv, etc...
 - Services en ligne
 - Developpeurs

## concurrents
 
 - liste
 - etat des lieux
 - comparaison
 - cdn intelligents: akamai

## technologies

 - nodejs: evented i/o, javascript
 - C++: manipulation
   - custom IO
   - Leptonica (Google dev) puis custom operations
 - pipeline
 - hooks
 - constraints
 - unit tested

## optimisations

 - pre-caching on idle
 - simd
 - custom allocators

## architecture

 - landing page + site commercial sur Github
 - app sur Joyent
 - cache sur Cloudflare

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

## communication

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
 
## planning

 - 6 mois
 - (details)
 
## besoins

 - fulltime
 - 1 ui/ux pour le site et l'interface d'admin
 
## questions?

## sources

 - http://ress.io
 - https://responsive.io
 - http://www.resrc.it
 - http://adaptive-images.com
 - http://www.sencha.com/learn/how-to-use-src-sencha-io
 - http://mobile.smashingmagazine.com/2013/10/24/automate-your-responsive-images-with-mobify-js/
 - https://developers.google.com/speed/articles/web-metrics