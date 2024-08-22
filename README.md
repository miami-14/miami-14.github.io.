
# Méthodes GET et POST
<div>
 la méthode GET doivent uniquement être utilisées afin de récupérer des données. La méthode HEAD demande une réponse identique à une requête GET pour laquelle on aura omis le corps de la réponse (on a uniquement l'en-tête). La méthode POST est utilisée pour envoyer une entité vers la ressource indiquée. 
(https://developer.mozilla.org/fr/docs/Web/HTTP/Methods)/
</div>

#  Comparaison méthodes
<div>
<table>
  
  <thead>
    <tr>
      <th scope="col">GET</th>
      <th scope="col">POST</th>
    </tr>
  </thead>
  <tbody>
    <tr>
 <thead>
  <tr>
  
 <th scope="row">Visible pour l’utilisateur dans le champ d’adresse</th>
 <td> Invisible pour l’utilisateur </td>
 
  </tr>
  </thead>

  <tr>
    <th scope="row">Les paramètres de l’URL sont stockés en même temps que l’URL  </th>
 <td> L’URL est enregistrée sans paramètres URL </td>
    </tr>
  </thead> 

   <tr>
    <th scope="row"> Les paramètres de l’URL sont stockés sans chiffrement   </th>
 <td> Les paramètres de l’URL ne sont pas enregistrés automatiquement  </td>
    </tr>
  </thead> 

  <tr>
    <th scope="row"> Les paramètres de l’URL ne sont pas envoyés à nouveau   </th>
 <td> Le navigateur avertit que les données du formulaire doivent être renvoyées  </td>
    </tr>
  </thead> 

  
  <tr>
    <th scope="row"> Caractères ASCII uniquement </th>
 <td> Caractères ASCII mais également données binaires </td>
    </tr>
  </thead> 

  
  <tr>
    <th scope="row">  	Limitée - longueur maximale de l’URL à 2 048 caractères </th>
 <td> Illimitée  </td>
    </tr>
  </thead> 

  </table>
</div>

#  Extensible

  Le protocole HTTP est extensible à plusieurs niveaux grâce à ses fonctionnalité bien de nouvelles  capacité avecles versions antérieures. Grâce a :
 - aux methodes HTTP personnalisées
 - En tête HTP personnalisés
 - Les types de contenu
 - code de statut HTTP étendus
 - extensions via WebSockets et HTTP/2
 - les versionnement du protocole
 - Utilisation de cookies et d'autres mécanismes de session.

   # Sans état 

Le protocole HTTP est qualifié de "protocole sans état" car chaque requête envoyée par un client à un serveur est indépendant des autres. autrement dit, le serveur ,ne conserve aucune information concernant les interactions précédentes avec le client une fois la requête traitée. Chaque requête est donc traitée comme une nouvelle interaction, sans référence à celle qui l'ont précédée. 
Par conséquences pour la navigation web : 
- Pas de persistance des données entre les requêtes
- Gestion des sessions 
- Scalabilité et simplicité ( l'absence d'état ) 


# URL 
- Le protocole (https://) 
- Le sous domaine (www.)
- Le nom de domaine principale ( mondomaine)
- Le domaine de deuxième niveau (.com)
- Le répertoire (/contact)


# Code Status 
Les codes les plus courants sont : 
- 200: succès de la requête 
- 301 et 302: redirection, respectivement permanente et temporaire 
- 401: utilisateur non authentifié 
- 403: accès refusé  
- 404: Ressource non trouvé  
- 500,502 et 503: erreurs serveur 
- 504: Le serveur n'a pas repondu

  # Négociation de contenu

Lorsqu'un client souhaite obtenir une ressource, il la demande via une URL. Le serveur utilise alors cette URL pour choisir l'une des variantes disponibles. Chaque variante est appelée une représentation. Le serveur renvoie alors une représentation donnée au client.


![httpnego](https://github.com/user-attachments/assets/04a1eb63-25ec-4c2d-9011-178685899731)


  



