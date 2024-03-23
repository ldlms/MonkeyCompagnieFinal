Projet réalisé pour le compte d'une auto-entreprise, dans le secteur de l'animation :

* Utilisation du framework PHP LARAVEL, couplé à la librairie Inertia.js,
* Views en vue.js

* BDD MariaDB

* Site vitriné constitué : 
* d'une page d'acceuil présentant l'équipe de l'entreprise
* d'une page affichant le programme du mois à venir 
* d'une galerie d'albums photos
* d'une page contact
* d'une page présentant des quizzs (vrai ou faux, qui est-ce, QCM), pour donner une idée des activitées présentées par l'entreprise

* D'un panel admin (crée en adaptant le package Breeze) permettant d'alimenter les différentes pages sus-citées

* SPA testée via le framework Cypress.js

---------------------------------------------------
Installation coté serveur :
Installer Laravel : composer global require laravel/installer
Installer inertia : composer require inertiajs/inertia-laravel
Installer le middleware : php artisan inertia:middleware

Installation coté client : 
Installation vue.js : npm install vue@next
Installation des dépendances : npm install @inertiajs/inertia @inertiajs/inertia-vue3

Lancer le projet
- configurer le fichier .env
- "npm run dev" ET "php artisan serve"


* Screenshots

* Page d'acceuil :
![image](https://github.com/ldlms/monkeyCompagnie/assets/123155110/2b400122-5f84-4326-8ee3-ce4d3484f4f5)


* Page  programme :
![image](https://github.com/ldlms/monkeyCompagnie/assets/123155110/cde41f47-1457-4f65-a4de-e04f382bd1f8)


* Page galerie :
![image](https://github.com/ldlms/monkeyCompagnie/assets/123155110/6311a7b2-a6d5-499e-af9f-de74e9151a89)


* Page contact :
![image](https://github.com/ldlms/monkeyCompagnie/assets/123155110/e7bb9569-a1be-4c71-9f15-55a6e5bec1c4)
![image](https://github.com/ldlms/monkeyCompagnie/assets/123155110/3a9b7d90-ef29-4fd3-a839-aef498c7d52e)



* Page quizz :
![image](https://github.com/ldlms/monkeyCompagnie/assets/123155110/c2c75323-b6dc-4e9d-93f8-2718744417fc)


* Exemple du panel admin :
![image](https://github.com/ldlms/monkeyCompagnie/assets/123155110/1008dd44-e401-4043-9d72-d65ca4eda1ae)

Exemple du site en version mobile :

![image](https://github.com/ldlms/monkeyCompagnie/assets/123155110/d3e28226-fe04-45e5-b606-98d581b24f7b)
![image](https://github.com/ldlms/monkeyCompagnie/assets/123155110/3e92a58c-b6b1-436a-b614-523d0dbd5ac4)




