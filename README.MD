
un workflow qui teste automatiquement un code Node.js du fichier "example.test.js" sur la VM Runner, l'action s'exécute suite au push.

=================

À chaque fois que tu fais un push sur GitHub, le workflow :

-Crée une machine virtuelle linux (appelée runner), par défaut ubuntu-latest dans le cloud GitHub.

-Clone le code NodeJS du dépôt GitHub dans le répertoire local du runner

-Installe les dépendances (npm install)

-Lance les tests (npm test)

-affiche dans git action le résultat de ce test.

-Supprime tout une fois fini

==================================================================

NODEJS/
├── package.json
├── test/
│   └── example.test.js
└── .github/
    └── workflows/
        └── node-test.yml

créer un repo : NODEJS

git remote -v
git remote set-url origin https://github.com/soufianetalibi/NODEJS.git

git init 
git add . 
git status
git commit -m "Initial commit"

git push -u origin master

================================

Comment tester le workflow à nouveau :
  git init 
  git add . 
  git status 
  git commit --allow-empty -m "workflow run again"
  git push  

