### Entraînement avec React.js


## __Préambule__ :
#### Te voilà prêt à démarrer. Si tu tentes la commande :

npm run dev

#### Tu constateras qu'il n'y a rien d'affiché. C'est normal : J'ai nettoyé le fichier App.jsx, et j'ai supprimé les fichiers .css. En résumé : il n'y a rien d'autre qu'une <div> parente, et un commentaire à l'intérieur.

#### Pour cet exercice, tu vas devoir créer un petit projet permettant d'afficher tous les Simpsons, et de les filtrer. Voici les étapes :

  ## 0. Voici le lien vers le template, pour que tu aies une idée visuelle de ce qui devra être créé :

  https://www.figma.com/file/3ApwhdewT0QqPHSxr1IRry/Untitled?type=design&node-id=0-1&mode=design&t=5P2kN4ZhZ5FSJE8F-0
 
  #### Tu peux commencer à créer ton architecture (l'organisation des fichiers), et le CSS qui sera associé à chaque composant. Je t'invite à installer et utiliser SCSS dans ton projet :

  *npm install sass*

  #### Il te faudra donc créer un dossier style dans le dossier src/, lequel contiendra toutes les feuilles de styles que tu créeras.

  ## 1. Petite aide pour composer l'architecture : Le composant App doit importer les composants suivants :
##    ---> Header;
##    ---> HomePage;
##    ---> ContactPage;
##    ---> Footer;

  ##  `*1.bis : __Rappel :__ C'est le composant HomePage qui sera le propriétaire des données provenant de l'API.`
  ## `*1.ter : __A ce stade...__ Tu devras créer le header et le footer par toi-même, conformément à la maquette.`
  ## `*1.quater : __Côté architecture...__ Dans le dossier src/, je t'invite à structurer les éléments comme suit: Tous les composants finissant par "Page" seront dans un dossier "pages/" ; Tous les composants qui seront visibles sur toutes les pages seront dans un dossier globals/` 

  ## 2. Dans le composant HomePage, tu vas désormais fetcher ce qui vient de l'API (je te donne le lien dans quelques instants). Pour cela, tu as deux solutions :
    💡 Télécharger la librairie __axios__ (npm install axios);
    💡 Utiliser la méthode fetch, qui est nativement présente en JavaScript.
  ### Si ta mémoire te fait défaut, ou si tu veux explorer, je t'invite à lire la documentation d'une des deux méthodes. Tu peux aussi remettre le nez dans les quêtes pour voir comment faire 😊

  ##  `*2.bis : __Le endpoint__ de l'API sera le suivant ; c'est cette adresse qu'il faudra interroger pour récupérer les données :`
##    ---> https://rickandmortyapi.com/api/character
  ## `* Comme tu peux le constater, on interroge le endpoint /character.`

  ### Tu es bloqué ? 🧐 Revisite tes quêtes, ou regarde sur internet comment on fetch des données en React.js.

  ## 3. Stocke ces données dans un state (ou variable d'état) nommé data.
  ###   `* 3.bis : A l'initialisation, la valeur du state doit être un tableau vide.`
  ###   `*3.ter : Un petit console.log te permettra de savoir si tu as bien récupéré les données ✅`

  ## 4. 🔍️ Désormais, il est temps de faire fonctionner ta mémoire 🧠, et de faire tes propres recherches. Ton objectif est de mapper le tableau de personnages de Rick and Morty, pour retourner une carte par personnage. Il est volontaire de ma part de ne pas te guider davantage, pour que ta réussite soit le résultat de tes recherches et de ta curiosité 😊
  ###   `*4.bis : Un petit indice tout de même : tu dois créer un composant Card, qui servira à représenter chaque cartes.`

  ## 5. ... Après cette longue phase de travail, tu devrais avoir une liste de cartes. Applique le style qu'il faut pour pour être au plus proche de la maquette.

  ## 6. Il est l'heure d'ajouter de l'intéractivité à ta page. Si tu ne l'as pas fait, tu peux créer un selecteur (cf. maquette). 

  ### `* 6.bis : Un exemple de User Story :`
  #### `[US-??] En tant qu'utilisateur, je veux pouvoir filtrer dynamiquement les cartes affichées dans la HomePage`

  ## 7. Rendus à la septième étape, il est temps de te concentrer sur la création du formulaire de contact. En d'autres termes, le site que tu es en train de créer doit laisser la possibilité par un utilisateur lambda de contacter le propriétaire.
  ### `* 7.bis : Ton formulaire n'envoie rien pour le moment, et c'est normal. Ce qu'on souhaite, c'est que les éléments soient physiquement présents sur l'image`
  ### `* 7.ter : Veille à ce que le formulaire soit esthétiquement cohérent avec les éléments designés sur la HomePage. Comme tu peux le constater, il n'apparaît pas sur la maquette. Tu as le champ libre pour le styliser à ta guise.`

  ## 8. Il est temps d'installer la dépendance suivante :
  `*    ---> npm install react-router-dom`
  ### Tu l'as compris : Il faut donner à l'utilisateur la possibilité de changer de page. Je te laisse replonger dans ce que tu as appris dans les quêtes concernant la navigation en React.js, et ses spécificités. Aussi, la documentation en ligne concernant la dépendance `* react-router-dom` est bien faite, et te donnera toutes les clés pour comprendre comment cela fonctionne 😀
  ### `* 8.bis : Lorsque l'utilisateur atteris sur la ContactPage, il lui faut pouvoir revenir sur la HomePage via un bouton explicite (tel qu'exposé sur la maquette)`
  ### `* 8.ter : La déclaration des routes peut être réalisée directement dans le fichier main.jsx. Tu peux aussi les déclarer dans un fichier à part, que tu pourrais appeler Router.jsx`

  ## 9. Nouvelle étape, nouveau palier difficulté : Les cartes doivent être cliquables, et renvoyer vers une page par id.
  ### `* 9.bis : Tu te rappelles de useParams ?`