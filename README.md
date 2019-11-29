# Platforme-Annonces
1. Récupérer le code
Vous avez deux solutions pour le faire :

 Via Git, en clonant ce dépôt ;
 Via le téléchargement du code source en une archive ZIP, à cette adresse
:https://github.com/Abdel-E-durable/Platforme-Annonces/archive/master.zip


2. Définir vos paramètres d'application

Pour ne pas qu'on se partage tous nos mots de passe, le fichier app/config/parameters.yml est ignoré dans ce dépôt. A la place, vous avez le fichier parameters.yml.dist que vous devez renommer (enlevez le .dist) et modifier.

3. Télécharger les vendors

 Avec Composer:
 php composer.phar install


4. Créez la base de données
Si la base de données que vous avez renseignée dans l'étape 2 n'existe pas déjà, créez-la :

php bin/console doctrine:database:create
Puis créez les tables correspondantes au schéma Doctrine :

php bin/console doctrine:schema:update --dump-sql
php bin/console doctrine:schema:update --force
Enfin, éventuellement, ajoutez les fixtures :

php bin/console doctrine:fixtures:load
5. Publiez les assets
Publiez les assets dans le répertoire web :

php bin/console assets:install web
Et profitez !
