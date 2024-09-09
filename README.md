
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
```
  Le protocole HTTP est extensible à plusieurs niveaux grâce à ses fonctionnalité bien de nouvelles  capacité avecles versions antérieures grâce a :
```
 - aux methodes HTTP personnalisées
 - En tête HTP personnalisés
 - Les types de contenu
 - code de statut HTTP étendus
 - extensions via WebSockets et HTTP/2
 - les versionnement du protocole
 - Utilisation de cookies et d'autres mécanismes de session.

   # Sans état 
```
Le protocole HTTP est qualifié de "protocole sans état" car chaque requête envoyée par un client à un serveur est indépendant des autres. autrement dit, le serveur ,ne conserve aucune information concernant les interactions précédentes avec le client une fois la requête traitée. Chaque requête est donc traitée comme une nouvelle interaction, sans référence à celle qui l'ont précédée. 
Par conséquences pour la navigation web :
```
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
```
Les codes les plus courants sont :
```
- 200: succès de la requête 
- 301 et 302: redirection, respectivement permanente et temporaire 
- 401: utilisateur non authentifié 
- 403: accès refusé  
- 404: Ressource non trouvé  
- 500,502 et 503: erreurs serveur 
- 504: Le serveur n'a pas repondu

  # Négociation de contenu
```
Lorsqu'un client souhaite obtenir une ressource, il la demande via une URL. Le serveur utilise alors cette URL pour choisir l'une des variantes disponibles. Chaque variante est appelée une représentation. Le serveur renvoie alors une représentation donnée au client.
```

![httpnego](https://github.com/user-attachments/assets/04a1eb63-25ec-4c2d-9011-178685899731)

# Installation Apache & configuration 

## Installation XAMPP 

```
étape 1 Installer XAMPP
```
![installation d'un logiciel ](https://github.com/user-attachments/assets/3414cd4f-74ab-4acd-8ea0-bacede1c0db6)

```
étape 2 Ouvir XAMPP
```

![XAMPP](https://github.com/user-attachments/assets/6faaa3c5-cb7d-464e-8faa-cde833debf65)


## Configuration un virtualhost sur votre poste local.
```
étape 1
``` 
![Virtualhost0](https://github.com/user-attachments/assets/6a540d99-dacf-40f7-8586-2af074c01f62)


```
étape 2
```
![virtualhost](https://github.com/user-attachments/assets/70e53bbf-1b70-4e12-af29-dffdd416f926)

```
étape 3
```
![Virtualhost1](https://github.com/user-attachments/assets/da0166dc-09f8-43a0-80b5-c652a32a63f6)


# CURL
```
 1.1 Mettre dans la commende " http://dev.local/download/test.txt "
```
![Capture d'écran 2024-09-03 094858](https://github.com/user-attachments/assets/1ad8e1e5-f922-414f-894a-7c4004d9d75b)

```
1.2 Aller dans ce pc. Puis aller dans le dossier XAMPP. Enfin dans le dossier htdoc
```
![Capture d'écran 2024-09-03 102637](https://github.com/user-attachments/assets/c9fc5452-3c2e-4077-8552-c0aad7061c72)

```
1.2 crérer un dossier "mkdir dir C:\xampp\htdocs\dev.local"
```
![Capture d'écran 2024-09-03 094921](https://github.com/user-attachments/assets/0139d73d-957c-4ade-a918-9afb936bbdcd)

```
 1.3 crerer un dossier "mkdir C:\xampp\htdocs\dev.local\download"
```
![Capture d'écran 2024-09-03 094931](https://github.com/user-attachments/assets/3c33ad8a-7723-4d35-9f60-f9ec7d2c6026)

```
 1.4 Crérer un dossier "dev.local"
```
![Capture d'écran 2024-09-03 102714](https://github.com/user-attachments/assets/717778c6-e28c-4bc3-83a7-265e5dda5fbc)

```
1.5 crerer un dossier "mkdir C:\xampp\htdocs\dev.local\download"
```
![Capture d'écran 2024-09-03 094931](https://github.com/user-attachments/assets/3c33ad8a-7723-4d35-9f60-f9ec7d2c6026)


```
1.6 Crérer un dossier "Download"
```
![Capture d'écran 2024-09-03 102724](https://github.com/user-attachments/assets/d03d8c02-24fc-4324-b5c5-11276e839568)


```
1.7 crérer un texte
```
![Capture d'écran 2024-09-03 102731](https://github.com/user-attachments/assets/1a9ac68f-6d38-4385-8f90-33d41e4dfdd1)


```
2 Vérifier que les créations fonctionnent
```
![Capture d'écran 2024-09-03 094938](https://github.com/user-attachments/assets/005f80f1-e952-4894-8f4c-3d68fe9dd01e)

```
3.1 Crerer un copie du texte
```
![Capture d'écran 2024-09-03 094956](https://github.com/user-attachments/assets/43890ab8-1c36-4939-8fce-1f451b244296)

```
3.2 Affichier dans le dossier dev.local
```
![Capture d'écran 2024-09-03 102724](https://github.com/user-attachments/assets/d03d8c02-24fc-4324-b5c5-11276e839568) 


```
4 "curl -O https://dev.local/index.html"
```
  ![Capture d'écran 2024-09-03 095038](https://github.com/user-attachments/assets/6f7b9431-88ec-4f4a-9420-adc1b8b7ccef)

```
5 Effectuer une requête GET vers l’url "http://dev.local " 
```
![Capture d'écran 2024-09-03 095106](https://github.com/user-attachments/assets/b4eaf9e9-09db-4e53-844b-11671dbbaec0)

```
6 Effectuer une requête GET vers l’url http://dev.local/notExisting
```
![Capture d'écran 2024-09-03 095112](https://github.com/user-attachments/assets/a5aa0b86-b29d-4e6e-8d83-19e0938a94dc)



# 10 – Headers


<div>
<table>
  
  <thead>
    <tr>
      <th scope="col">En-tête	</th>
      <th scope="col">Description</th>
     <th scope="col">Exemple</th>
    </tr>
  </thead>

  

  </tbody>
   <tr>
    <th scope="row"> Host </th>
    <th scope="row">Spécifie le nom de domaine du serveur (et le numéro de port, si nécessaire). </th>
    <th scope="row"> www.example.com  </th>
 
  </tr>
 

 

  <tr>
    <th scope="row">User-Agent	 </th>
    <th scope="row"> Fournit des informations sur le client utilisateur, telles que le navigateur et le système d'exploitation.  </th>
    <th scope="row"> User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) </th>

  </tr>
 
    

   <tr>
    <th scope="row"> Accept </th>
    <th scope="row"> Indique les types de contenu que le client est capable de traiter. </th>
    <th scope="row"> Accept: text/html, application/json </th>
 
   </tr>
  

  

  <tr>
    <th scope="row"> Accept-Encoding	 </th>
    <th scope="row"> Spécifie les encodages de contenu que le client est capable de décompresser.	</th>
    <th scope="row"> Accept-Encoding: gzip, deflate, br </th>
    
   </tr>
   

   
  <tr>
    <th scope="row"> Accept-Language	 </th>
    <th scope="row"> Indique la langue préférée du client pour le contenu de la réponse. </th>
    <th scope="row"> Accept-Language: en-US, fr-FR;q=0.8 </th>
   
   </tr>
  

  
  <tr>
    <th scope="row"> Authorization	 </th>
    <th scope="row"> Transmet des informations d'authentification pour accéder à une ressource protégée.	 </th>
    <th scope="row"> Authorization: Basic dXNlcm5hbWU6cGFzc3dvcmQ= </th>
 </tr>
  

  
 
 <tr>
    <th scope="row"> Cookie	 </th>
    <th scope="row"> Envoie les cookies précédemment définis par le serveur au client.	</th>
    <th scope="row"> Cookie: sessionId=abc123; lang=fr </th>
 </tr>
 

 

 <tr>
    <th scope="row"> Content-Type	</th>
    <th scope="row"> Indique le type de média de la ressource envoyée (lorsque la requête contient un corps, comme POST).	 </th>
    <th scope="row"> Content-Type: application/json </th>
 </tr>



 <tr>
    <th scope="row"> Content-Length			 </th>
    <th scope="row"> Spécifie la longueur du corps de la requête en octets.	 </th>
    <th scope="row"> Content-Length: 348</th>

 </tr>


 
 <tr>
    <th scope="row"> Referer	</th>
    <th scope="row"> Indique l'URL de la page précédente à partir de laquelle la requête a été faite.		 </th>
    <th scope="row"> Referer: https://www.google.com/ </th>
 </tr>
 


 <tr>
    <th scope="row"> Connection	</th>
    <th scope="row"> Indique si la connexion doit être maintenue ouverte après l'envoi de la réponse.	 </th>
    <th scope="row"> Connection: keep-alive </th>
 </tr>



 <tr>
    <th scope="row"> Cache-Control		</th>
    <th scope="row"> Fournit des directives de mise en cache spécifiques pour les caches en aval.	 </th>
    <th scope="row"> Cache-Control: no-cache </th>
 </tr>




 <tr>
    <th scope="row"> Upgrade-Insecure-Requests	</th>
    <th scope="row"> Indique au serveur que le client préfère une version sécurisée (HTTPS) de la ressource demandée.	</th>
    <th scope="row"> Upgrade-Insecure-Requests: 1 </th>
 </tr>

</tbody>

  </table>
</div>



