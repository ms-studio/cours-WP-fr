WordPress Courseware
***********************
Pour débuter:

Décider si vous utilisez le service WordPress.com ou une installation indépendante (WordPress.org).

Pour ouvrir un site sur WordPress.com, il vous suffit d'ouvrir un compte [ici](https://fr.wordpress.com/signup/).

Les particularités de WordPress.com:

- Un choix "limité"* de thèmes gratuits ou payants (de 60 à 130$): [http://theme.wordpress.com/](http://theme.wordpress.com/) (*tout de même plus de 200...)
- Vous ne pouvez pas installer de plugins.
- Il faut [payer un supplément](http://en.support.wordpress.com/upgrades/) pour un nom de domaine personnel ($18/année), ou pour effectuer des modifications graphiques ($30/année). Pour un site quelque peu personnalisé (domaine personnel, ajustements graphiques, sans bannière publicitaire), il y a [un bundle de 99$](http://store.wordpress.com/bundles/).
- les mises à jour sont effectuées automatiquement, vous n'aurez pas à vous en soucier.

Avec une installation indépendante:

- Vous devez payer le nom de domaine et l'hébergement.
- Vous avez le choix parmi des milliers de [thèmes](http://wordpress.org/themes/) gratuits ou payants.
- Vous pouvez installer librement des [plugins](http://wordpress.org/plugins/) pour ajouter des fonctionalités.
- Vous devrez appliquer les mises à jour régulièrement.

La suite de ce chapitre concerne uniquement l'option 2: un site WordPress indépendant.

Pour créer un site indépendant, vous devez disposer de deux choses:

1. Un nom de domaine.
2. Un hébergement.

Obtenir le nom de domaine
*************************

Note: certains hébergeurs vous offrent un nom de domaine inclus dans l'hébergement. Cela va toutefois vous lier à cet hébergeur, il pourra être compliqué de conserver ce nom de domaine si vous changez d'hébergement.

Pour obtenir un nom de domaine, il faut passer par un "registrar", un service d'enregistrement. 

Pour les noms de domaines en ".ch", il y a un registrar unique: [http://nic.ch](http://nic.ch)

Le prix pour un ".ch" est de 17.- chf/année.

Pour les domaines ".com", ".org", ".net", le prix est d'à peu près 10.- dollars/année. Pour les autres domaines - ".info", ".io", ".fm", ".tv"... - cela varie, il faut chercher.

Il n'y a pas de différence "qualitative" entre un registrar et un autre.

J'utilise personnellement le registrar GKG.net. En France, Ghandi est un registrar très connu.

La procédure:

- Vérifiez si le nom de domaine est disponible.
- Procédez à l'achat, pour le nombre d'années que vous souhaitez.
- Ne souscrivez pas à des services inutiles qu'on essayera peut-être de vous vendre...

Obtenir un hébergement
**********************
Contrairement au choix du registrar, le choix de l'hébergement est plus délicat, car la qualité varie d'un prestataire à l'autre, et un mauvais choix signifie:

- Temps de chargement lent.
- Site trop fréquemment inaccessible.
- Problèmes lors des mises à jour de WordPress ou de plugins. 

Ces problèmes ne se détectent qu'à l'usage, il est donc utile de se renseigner auprès d'usagers expérimentés.

Les critères objectifs qui peuvent orienter un choix:

- Le prix.
- L'hébergement permet-il d'utiliser plusieurs domaines, ou un seul?
- L'hébergement comprend-il des services de mailing-liste ou newsletter?
- Les utilisateurs du site seront-ils en Europe, ou sur un autre continent?
- L'espace de stockage.

L'espace de stockage est souvent le critère le moins important. Les hébergeurs offrent souvent des dizaines de gigas d'espace. Avec un site WordPress normal, il vous faudra des milliers d'images pour arriver à remplir 1 ou 2 gigas.

Le choix d'un hébergement aux Etat-Unis ou en Europe devrait dépendre du public cible. Il y a un temps de latence entre les continents, et Google peut favoriser les résultats géographiquement proches.

Si on n'a pas envie de faire des tests comparatifs, je conseille un hébergement chez Hostpoint.ch. De mon expérience, ils ont des réglages optimaux pour WordPress, sans qu'il y ait des soucis de permissions sur les répertoires, souvent rencontrés ailleurs. De plus, [leurs offres](https://www.hostpoint.ch/fr/herbergement-web/herbergement-apercu.html) permettent d'avoir plusieurs noms de domaines.

Si vous cherchez moins cher, mon conseil est: évitez d'aller chez un hébergeur bas de gamme, vous perdrez du temps avec divers soucis techniques. Associez-vous plutôt avec d'autres personnes pour partager un même hébergement de qualité.

Les Name Servers
***************** 

Une fois l'hébergement acheté, vous recevrez un courriel contenant le lien vers l'interface admin, avec nom d'utilisateur et mot de passe.

Il vous faudra parcourir la documentation, pour trouver quels sont les "Name Servers" de votre hébergeur.

Il s'agit généralement de 3 URL, ressemblant à ceci (pour Hostpoint).

- ns.hostpoint.ch
- ns2.hostpoint.ch
- ns3.hostpoint.ch

Pour faire pointer votre nom de domaine vers votre hébergement il faut retourner dans le panneau d'administration du registrar, et faire une modification DNS du domaine. Vous aurez la possibilité d'entrer les "Name Servers" voulus.

La base de données
******************

A présent, il reste à configurer une base de données (c'est elle qui contiendra le texte de vos articles). Rendez-vous dans le panneau d'administration de l'hébergeur, et cherchez l'endroit permettant de configurer une base de données. Il vous faudra:

- Créer une base de données (de type MySQL).
- Créer un utilisateur ayant les droits admin sur cette base.
- Inventez un mot de passe long et compliqué.

Il est temps de créer un document rassemblant les divers codes d'accès dont vous aurez besoin.

Notez dans ce document:

- L'accès à l'admin du registrar
- L'accès à l'admin de l'hébergement
- L'accès FTP
- L'accès à la base de données
- Les utilisateurs admin WordPress

Vous pouvez télécharger un fichier d'exemple ici: [Infos_Site_WordPress.rtf](Infos_Site_WordPress.rtf)
 
Installation de WordPress
*************************

Afin de procéder à l'installation, 
procurez-vous la version la plus récente de WordPress:
 
- En anglais: 
- En français: 

Décompactez le zip. Vous obtiendrez un dossier nommé "wordpress".

En utilisant un logiciel FTP, uploadez le contenu du dossier "wordpress" à la racine de votre hébergement web.

Votre logiciel FTP vous demandera: 
- Le nom du serveur: entrez votre domaine.
- Le nom utilisateur et le mot de passe.

Conseils avec CyberDuck: 
- cochez "Add to Keychain" pour ne pas entrer le mot de passe à chaque fois.
- une fois la connexion ouverte, créez un signet (bookmark), cela vous permettra d'ouvrir la connexion par un simple clic.

Une fois que tous les fichiers de WordPress ont été copiés sur votre serveur, entrez l'adresse de votre domaine dans un navigateur.

Vous pourrez alors débuter l'installation de WordPress.

Suivez les consignes affichées à l'écran, et entrez les accès de base de donnée.

Les points importants:

- Changez le préfixe de la base de données (par défaut wp_) par exemple en wp1_. Cela améliore la sécurité de votre site.
- Lorsque vous créez l'utilisateur admin, donnez-lui un nom autre que "admin".
- Donnez à cet utilisateur un mot de passe très complexe et très long. Si vous tenez à un mot de passe simple, vous pourrez créer plus tard un utilisateur avec le statut "Editeur". 

L'installation à réussi? C'est parfait, vous pouvez à présent commencer à entrer vos contenus...

*********

Support de cours WordPress
Octobre 2013
Licence: CC-BY-SA

Vous pouvez télécharger ce support de cours aux emplacements suivants:

- github: 
- dropbox: 
- bittorrent sync: 