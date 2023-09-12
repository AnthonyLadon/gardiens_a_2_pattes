# Gardiens à 2 pattes 🐶

Projet de fin d'études que j'ai présenté à l'Institut Saint Laurent pour mon diplôme de web developer

## 🚀 Pour tester le projet en local

# Projet Bien-être

Le site est un annuaire où des prestataires peuvent s’inscrire gratuitement et mettre en avant leurs services dans le domaine du bien-être.

## ✍️ Auteur

- [@AnthonyLadon](https://www.github.com/anthonyladon)

## 🚀 Pour installer le projet

- Prérequis:

  - php 7.2.5 ou >
  - composer (https://getcomposer.org/download/)
  - Un gestionnaire de base de données (MySQL, Postgresql..)

- Puis lancez les commandes suivantes:

```bash
$ git clone https://github.com/AnthonyLadon/gardiens_a_2_pattes.git

se positionner dans le repertoire du projet:
$ cd gardiens_a_2_pattes/

installer les dépendances:
$ composer install
```

- Configurer l'accès à la DB dans le fichier ".env" situé à la racine du projet. Modifiez 'nom_DB' et 'mot_de_passe' (ainsi que l'adresse du localhost si besoin)

```
DATABASE_URL="mysql://nom_DB:mot_de_passe@127.0.0.1:8889/bienetre?serverVersion=8&charset=utf8mb4"
```

- Configurer le mailer dans le fichier ".env" (Pour ce projet j'ai utillisé Mailtrap -> https://mailtrap.io)

Lancez la commande pour créer la base de données

```bash
$  php bin/console doctrine:database:create
```

Lancez les migrations (création des tables + realtions dans la DB)

```bash
$  php bin/console d:m:m
```

Lancer les fixutes (insertion de données dans la base de données (Codes postaux, villes..)) Attention ceci purge la base de données avant insertion !

```bash
php bin/console doctrine:fixtures:load
```

- Démarrer le serveur Symfony

```bash
$  symfony server:start
```

## Variables d'environnement

Pour faire tourner ce projet vous devez ajouter ces variables d'environnement dans le fichier ".env":

`MAILER_DSN`"votre mailer"` voir documentation officielle Symfony

Une clé API Stripe (mode test)
`STRIPE_SECRET_KEY=`
`STRIPE_PUBLIC_KEY=`

Une clé API Google Oauth
`GOOGLE_CLIENT_ID=`
`GOOGLE_CLIENT_SECRET=`

#### - Pour effectuer un paiement (Mode test de STRIPE):

- Carte VISA: 4242 4242 4242 4242
- Date: 12/26
- Code CVC: 123

## 🧑‍🔧 Tech Stack

**Client:** Javascript, Jquery, Twig, Sass, Materialize CSS

**Server:** PHP, Symfony Framework

**API's & external services:** OpenCage (Geocoding API), Stripe API, Google OAuth 2.0 API, Mailtrap, SurveyMonkey

- https://opencagedata.com/ (Geocoding)

## ✍️ Auteur

- [@AnthonyLadon](https://www.github.com/anthonyladon)
