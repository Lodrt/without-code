# deployer-une-app-sans-code
## TD maxime petitjean

### Question 4

$vercel -v 

La commmande retourne : Vercel CLI 21.1.0 \21.1.0

### Question 5 

$vercel init 

### Question 6 

$vercel 

### Question 7 

$vercel ls

### Question 8 

$vercel log angular-m8evznq82.vercel.app

### Question 9

https://vercel.com/docs/cli#commands/inspect

sur la documentation du cli on peut donc voir que versel inspect [unique-deployment-url] permet de retourner les informations à propos d'un déploiement spécifique

donc on peut y voir l'id, le name, l'état, l'url 

ainsi que les builds et les routes 

### Question 10 

Les variables d'environnements permettent de séparer le configuration requise par un environnement de production de celle requise par un environnement de développement.
Par exemple elles peuvent être utilisées pour renseigner la configuration d'une base de données ou pour définir des mots de passe.

L'intérêt c'est donc d'éviter de stocker des informations sensibles au sein de l'application et de pouvoir les séparer.

### Question 11

$vercel env add plain TEXT 

j'aurai pu ajouter la variable env qu'à la production avec par exemple : 

vercel env add plain TEXT production 

### Question 12  

$vercel env ls 

me retourne la variable que j'ai créé avant.

### Question 13


https://vercel.com/docs/cli#commands/secrets

vercel secrets permet donc de gérer les secrets utilisé dans les variables d'environnement. 
Comme par exemple le mdp d'une base de données.


### Question 15

j'ai d'abord fait un $vercel env pull 
pour rappatrier la variable que j'avais faite sur le site web

je créer un secret 

$vercel secrets add monsecret 562fgdfgmslkj;

puis je créer une variable d'environnement avec ce secret
 
$vercel env add secret EXAMPLE_SECRET1 production;
$monsecret

et voila mon secret monsecret et associé à la variable d'environnement EXAMPLE_SECRET1

### Question 16

automatiquement on a comme environnements : production | preview | development 

ces environnements nous permettent de partionner nos travaux et donc de garder tout ce qui touche au developpement dans l'environnement de dev etc.

### Question  18

https://without-code-ten.vercel.app/

### Question 19

les pull request sont une fonctionnalité facilitant la collaboration : c'est une demande de pull 


voir screenshoot.png

vercel deploie automatiquement la pull request sur le projet angular et whitour-code sur un environnement de priview


### Question 20 

une fois la pull requuest approuvée l'environnemnet de production est alors trigger.

### Question 21 

l'environnement de producution correspond à la branch main (on peut choisir la branch dans les réglages).
l'intérêt d'utiliser les pull requests sur un projet est de pouvoir tester le code dans des preview pour pouvoir savoir comment celui-ci réagis et s'il ne pose pas de problèmes avant de le passer en production (donc de le merge sur la branche principale).

Le workflow est donc : création d'une branch / développment de la feature / push sur github / pull request / tests / validation / merge

### Question 22

Le serverless est un modèle de cloud computing dans lequel le client peut créer / executer ses applications sans se soucier de la partie infrastructure et notamment la partie serveur. 
Evidemment cela continue de s'éxecuter sur un serveur mais le développeur doit juste fournir son code et tout le reste est à la charge du fournisseur du service cloud. 
L'intérêt est donc que le développeur va pouvoir se concentrer uniquement sur son travail. 

Pour rentrer dans le modèle serverless : le code d'éxecution doit être décomposer en fonction.
C'est l'ensemble de ces fonctions qui constitue l'application : Function As A Service : FAAS.

Les fonctions sont déclanchées par des événements. Exemple : Déclencheur -> requête http


