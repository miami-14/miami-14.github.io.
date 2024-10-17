## Informations 

- [Le modèle OSI](#Le-modèle-OSI)
- [](#)
- [](#)







# Le modèle OSI


## 1- Les origines du modèle OSI

`Le modèle OSI` (****Open Systems Interconnection****), proposé par l'ISO (****International Organization for Standardization****) en 1984, est un modèle de référence à sept couches conçu pour structurer l'interconnexion de systèmes ouverts. Bien que les protocoles spécifiques de l'OSI soient aujourd'hui considérés comme obsolètes, notamment avec la prépondérance d'Ethernet et IP, ce modèle reste un cadre de référence fondamental pour de nombreux standards et un langage commun pour les professionnels du réseau.


`Le modèle OSI` ne cherche pas à spécifier des technologies ou des moyens d'interconnexion particuliers, mais vise à décrire `les principes de communication externe entre systèmes`. Un système est dit "ouvert" s'il respecte ces principes dans ses échanges. L’objectif principal du modèle est d'offrir une base commune permettant de coordonner l'élaboration des normes d'interconnexion de systèmes et de positionner les normes existantes dans ce cadre.



Il est important de noter que le modèle OSI n'est pas conçu pour être une spécification technique ou une base d'évaluation des implémentations réelles. Il s'agit plutôt d'un cadre conceptuel permettant aux équipes d’experts de travailler sur des normes indépendamment pour chaque couche, favorisant ainsi une approche productive et standardisée du développement des systèmes d'interconnexion.


## 2. OSI, vue d’ensemble

`Le modèle OSI` est composé de sept couches. La liste suivante indique à la fois le nom des couches en français et en anglais :

![image](https://github.com/user-attachments/assets/fdc99019-f33e-41a2-9324-07eb114aa426)

Chacune de ces couches sera décrite par la suite afin de comprendre les fonctions qui y sont hébergées.

`Le modèle OSI` empile sept couches d’activité mais établit une frontière nette entre ce qui relève du transport des données et ce qui relève de leur traitement.

Les professionnels du réseau sont principalement concernés par les quatre couches inférieures.

![image](https://github.com/user-attachments/assets/dca559e5-62ba-49a3-80b3-c4991b7f8433)



### 1 - La couche Physique

`La couche Physique` est la première couche du `modèle OSI`  (****Open Systems Interconnection****), qui est un modèle de référence en sept couches pour la communication entre systèmes informatiques. Cette couche est responsable de la transmission physique des données sous forme de signaux électriques, optiques ou radio entre les dispositifs d’un réseau. 
- ****Par exemple**** Ethernet, Wi-fi, Bluetooh, fibre optique. 



### Fonctions principales de la couche Liaison de données :
 


| Nom | Son rôle | 
|-----|-----| 
|Transmission de bits|c'est la transmission de bits (0 et 1) entre deux appareils connectés. Ces bits sont transmis sous forme de signaux.|
|Médium de transmission|La couche Physique définit les types de supports physiques utilisés pour la communication ( câble en cuivre, fibre optique, ondes radio )|    
|Caractéristiques des signaux|  Amplitude, fréquence, phase pour les signaux analogiques et Le voltage pour les signaux électriques|
|Topologies physiques|Elle définit la manière dont les dispositifs sont physiquement interconnectés (bus, étoile, anneau, etc.).| 
|Synchronisation des bits|Assure que l’émetteur et le récepteur sont synchronisés pour interpréter les données correctement.|
|Débit de transmission|La couche Physique spécifie la vitesse à laquelle les données peuvent être envoyées (bits par seconde).| 
 

--------------------------------------  

### 2 - La couche Liaison de données

`La couche Liaison` de données est la deuxième couche du modèle OSI. Son rôle principal est d’assurer un transfert de données fiable entre deux nœuds adjacents dans un réseau, en détectant et en corrigeant les erreurs qui pourraient survenir lors de la transmission au niveau de la couche Physique.


### Fonctions principales de la couche Liaison de données :
 

| Nom | Son rôle| 
|-----|---------| 
| Encadrement (framing| La couche Liaison segmente les données en blocs appelés trames (ou frames) avant leur envoi. Chaque trame contient les données à transmettre ainsi que des informations de contrôle pour permettre la gestion et la vérification de la transmission.| 
|Adressage physique (MAC)|  Elle assure l'identification des dispositifs sur le réseau à l'aide des adresses physiques MAC (Media Access Control). Chaque appareil sur un réseau possède une adresse MAC unique qui permet de les identifier à ce niveau.| 
|Détection et correction d'erreurs|  La couche Liaison de données intègre des mécanismes pour détecter les erreurs de transmission, tels que les bits de contrôle (CRC – Cyclic Redundancy Check), et, dans certains cas, corriger ces erreurs avant que les données ne soient envoyées à la couche supérieure.|
|Contrôle de flux| Elle régule le flux des données entre deux appareils pour éviter qu’un récepteur soit submergé par trop de données à la fois.| 
| Accès au support (MAC) |  Elle définit des règles pour décider quand et comment les dispositifs peuvent accéder au médium de transmission. Par exemple, dans un réseau Ethernet, le protocole CSMA/CD (Carrier Sense Multiple Access with Collision Detection) est utilisé pour éviter les collisions lors de la transmission de données.|
| Fiabilité de la transmission| La couche Liaison garantit que les données arrivent correctement et dans l’ordre. Si des erreurs sont détectées dans une trame, elle peut demander la retransmission de la trame concernée.| 



### Sous-couches de la couche Liaison de données est divisé en deux :

|Sous-couche LLC (Logical Link Control) | Sous-couche MAC (Media Access Control)
|-------|------| 
|Gère le contrôle de flux, la détection d’erreurs et l’encapsulation des données venant des couches supérieures.| Gère l'accès au médium de transmission, c'est-à-dire qui peut transmettre et à quel moment, et contrôle l’envoi et la réception des trames.|
|Elle fournit des services à la couche Réseau, indépendamment du type de technologie de la couche Physique.|Responsable de l'adressage MAC.|


### Protocoles associés à la couche Liaison de données :

- Ethernet (câblé, standard IEEE 802.3)
- Wi-Fi (sans fil, standard IEEE 802.11)
- PPP (Point-to-Point Protocol)
- HDLC (High-Level Data Link Control)

### Exemples d'utilisation :

- Lorsque vous envoyez un fichier à une imprimante sur un réseau local, la couche Liaison garantit que les données arrivent à l'imprimante sans erreurs.

- Dans un réseau Wi-Fi, la couche Liaison de données s'occupe de la gestion des collisions et de l’accès partagé au médium sans fil.


---------------------------

### 3 - La couche Réseau

`La couche Réseau` est la troisième couche du modèle OSI, et son rôle principal est de gérer le routage et le transfert des données entre différents réseaux, en assurant que les paquets de données atteignent leur destination finale, même s’ils doivent traverser plusieurs réseaux intermédiaires.


### Fonctions principales de la couche Réseau :

| Nom | Son rôle| 
|-----|-------| 
|Routage | La fonction la plus importante de cette couche est de déterminer le meilleur chemin pour transmettre les paquets de données d'un nœud à un autre. Cela inclut la gestion des routes entre les réseaux locaux et distants, en utilisant des algorithmes de routage (ex: OSPF, BGP, RIP).| 
|Adressage logique (IP)|  Contrairement à la couche Liaison qui utilise des adresses MAC, la couche Réseau utilise des adresses IP (Internet Protocol) pour identifier de manière unique chaque dispositif sur un réseau global, ce qui permet la communication au-delà des réseaux locaux.| 
|Fragmentation et réassemblage des paquets| Si la taille d’un paquet de données dépasse la capacité maximale d'une liaison, la couche Réseau peut le fragmenter en plusieurs morceaux et ensuite les réassembler à destination.| 
|Interconnexion des réseaux |  La couche Réseau permet à différents réseaux de communiquer entre eux en utilisant des routeurs, qui relient des réseaux locaux (LAN) à des réseaux étendus (WAN) ou à l'Internet.|
|Contrôle de congestion| Pour éviter une surcharge du réseau, la couche Réseau peut mettre en œuvre des mécanismes de contrôle de la congestion, en ajustant le flux de données lorsqu’un réseau est saturé.|
|Gestion des erreurs et diagnostics| Cette couche permet également de surveiller le réseau, de détecter les pannes ou les erreurs, et de générer des messages de diagnostic (par exemple, avec le protocole ICMP, utilisé par la commande ping).| 

### Protocoles associés à la couche Réseau :

| Nom | Son rôle | 
|-----|-------| 
|IP (Internet Protocol)| C'est le protocole fondamental de cette couche, qui se divise en deux versions majeures :IPv4 : La version la plus utilisée, avec des adresses de 32 bits./IPv6 : Une version plus récente, avec des adresses de 128 bits, qui résout le problème de pénurie d'adresses IPv4.  | 
| ICMP (Internet Control Message Protocol)| Utilisé pour envoyer des messages d'erreurs et des informations de diagnostic, comme les commandes ping ou traceroute.|
|ARP (Address Resolution Protocol) | Utilisé pour associer les adresses IP aux adresses MAC au sein d’un réseau local.| 
|RIP, OSPF, BGP | Ce sont des protocoles de routage qui permettent aux routeurs de partager des informations sur les chemins possibles pour acheminer les paquets à travers les réseaux.|

### Exemples d'utilisation :

- Lorsque vous accédez à un site web, la couche Réseau permet de router les paquets de données depuis votre ordinateur, à travers divers routeurs et réseaux, jusqu’au serveur du site web.

- Dans un réseau d'entreprise, les routeurs gèrent le trafic entre les différents sous-réseaux pour acheminer correctement les données entre les utilisateurs et les serveurs.

### Différence avec les couches inférieures :

- La couche Physique gère l’envoi des bits bruts sur un support physique.
  
- La couche Liaison s’assure que les trames de données sont transmises correctement au sein d’un réseau local.
  
- La couche Réseau, quant à elle, gère les paquets de données et s’occupe de leur transport entre différents réseaux, souvent à grande échelle, comme sur l’Internet.


--------------------------------

### 4 - La couche Transport

`La couche Transport` est la quatrième couche du modèle OSI (Open Systems Interconnection) et joue un rôle crucial dans la communication entre des systèmes distants sur un réseau. Elle se situe entre la couche Réseau (couche 3) et la couche Session (couche 5) et est responsable de la gestion de la transmission de données de bout en bout entre deux machines.

| Nom | Son rôle | 
|-----|-------| 
| Segmentation et réassemblage |La couche Transport segmente les données en paquets (ou segments) de taille appropriée pour être envoyés sur le réseau. Ensuite, elle réassemble ces segments une fois arrivés à destination.|
| Contrôle de flux |Elle régule le flux de données pour éviter de surcharger le récepteur en envoyant trop de données à la fois. Le protocole TCP, par exemple, utilise des mécanismes comme le contrôle de congestion. |
| Contrôle d’erreurs |La couche Transport assure que les données sont envoyées sans erreur et dans le bon ordre. Elle effectue la vérification des erreurs et peut demander la retransmission des segments corrompus ou manquants. | 
| Multiplexage et dé-multiplexage | Elle permet à plusieurs applications sur un même hôte d’utiliser le réseau simultanément en distinguant les connexions grâce à des ports. Chaque application utilise un port spécifique pour communiquer via TCP ou UDP.|
| Connexion orientée ou non | Selon le protocole utilisé (par exemple, TCP ou UDP), la couche Transport peut établir une connexion fiable et orientée connexion (comme TCP), ou offrir un service de communication non orienté connexion, moins fiable mais plus rapide (comme UDP).| 


### Les deux principaux protocoles de la couche Transport

| TCP (Transmission Control Protocol) |UDP (User Datagram Protocol)| 
|-----|-------| 
| C'est un protocole orienté connexion qui garantit la livraison des paquets dans l'ordre et sans erreur. Il est utilisé pour des applications nécessitant une grande fiabilité, comme le web (HTTP), le courrier électronique (SMTP), ou le transfert de fichiers (FTP).| C'est un protocole non orienté connexion, plus léger et plus rapide que TCP, mais sans garantie de livraison ou d'ordre. Il est utilisé dans des applications où la vitesse est prioritaire sur la fiabilité, comme la diffusion en continu (streaming), les jeux en ligne ou les appels VoIP.| 

![image](https://github.com/user-attachments/assets/01a36943-0f63-4a76-a5f2-927a2a1e0056)

### 5 - La couche Session

`La couche Session` est la cinquième couche du modèle OSI (Open Systems Interconnection) et elle est chargée de gérer les sessions entre les applications qui communiquent sur le réseau. Une "session" est essentiellement une connexion logique établie entre deux dispositifs ou applications pour permettre l'échange de données.

### Les principales fonctions de la couche Session 

| Nom | Son rôle| 
|----|------|
|Gestion des dialogues (ou dialogues de communication)|  La couche Session organise et synchronise le dialogue entre deux applications. Elle établit, maintient et termine les sessions de communication. Cela signifie qu'elle garantit que les deux parties peuvent échanger des données de manière ordonnée.|
|Contrôle de la synchronisation | Elle permet l'ajout de points de synchronisation (ou de "checkpoints") dans la communication, ce qui facilite la reprise des échanges en cas de panne ou d'interruption. Par exemple, si une session est interrompue, la couche Session peut décider de redémarrer à partir du dernier point de contrôle, plutôt que de recommencer depuis le début.| 
| Ouverture, fermeture et gestion de sessions|La couche Session s’assure que les sessions sont correctement ouvertes et fermées. Elle peut gérer plusieurs sessions actives en même temps et assurer qu'elles fonctionnent correctement sans interférer les unes avec les autres.
| Contrôle du jeton (Token Management)| Dans certaines communications, la couche Session peut gérer un mécanisme de jeton (token), où une seule partie peut envoyer des données à un moment donné, pour éviter des collisions ou des conflits de communication.| 
|Rétablissement après erreur| Si une session est interrompue de façon inattendue, la couche Session peut être responsable de reprendre la communication à partir de là où elle s'était arrêtée.|

### Exemples d’utilisation de la couche Session :
| Protocole NetBIOS |RPC (Remote Procedure Call)| 
|-----|------| 
|Ce protocole, utilisé dans des réseaux locaux, fonctionne à la couche Session en permettant à des applications d'établir une session de communication et de s'authentifier.| Les appels de procédure à distance, utilisés pour exécuter des fonctions sur des systèmes distants, s'appuient sur la couche Session pour gérer les connexions.| 



### 6 - La couche Présentation

`La couche Présentation` est la sixième couche du modèle OSI (Open Systems Interconnection). Elle est parfois appelée la couche de traduction, car son rôle principal est de s'assurer que les données envoyées par une application sur un réseau peuvent être comprises par l'application réceptrice, même si ces applications utilisent des formats de données différents.

### Les fonctions principales de la couche Présentation

| Nom | Son rôle |
|------|-----| 
|Traduction des formats de données| Les systèmes différents peuvent utiliser des formats de données distincts. La couche Présentation traduit les formats utilisés par les applications en un format standardisé pour que les données puissent être échangées de manière compréhensible. Par exemple, elle peut convertir des données du format ASCII vers EBCDIC.| 
|Cryptage et décryptage| Si des données doivent être échangées de manière sécurisée, la couche Présentation prend en charge le chiffrement avant la transmission et le déchiffrement à la réception. C’est à ce niveau que les algorithmes de cryptage (comme SSL/TLS) sont souvent implémentés.|
|Compression des données|Pour améliorer l'efficacité de la transmission, cette couche peut compresser les données avant qu'elles ne soient envoyées sur le réseau et les décompresser à la réception. Cela permet d'optimiser la bande passante et d'accélérer la transmission.|  
|Gestion des formats multimédia| La couche Présentation s'occupe également de la gestion des formats multimédia, tels que les images, les vidéos et le son. Elle s'assure que les fichiers multimédias envoyés dans un certain format sont correctement interprétés et affichés par la machine réceptrice.|

### Exemples d'utilisation de la couche Présentation :

|JPEG, GIF, PNG| SSL/TLS|
|----|-----| 
|Ces formats de fichiers d'images sont interprétés à la couche Présentation. Les données binaires d’une image sont traduites en données compréhensibles pour les applications.| Les protocoles de sécurisation des communications sur Internet (comme HTTPS) fonctionnent en grande partie à la couche Présentation pour chiffrer et déchiffrer les données échangées entre un client et un serveur.|




### 7 - La couche Application 

`La couche Application` est la septième et dernière couche du modèle OSI (Open Systems Interconnection). C’est celle qui est la plus proche de l’utilisateur final et des applications réseau. Son rôle principal est de fournir des interfaces et des services pour les applications logicielles qui doivent communiquer à travers le réseau. Contrairement aux couches sous-jacentes, la couche Application ne traite pas directement la transmission des données, mais gère l’interaction entre l’utilisateur et l’application réseau.

### Fonctions principales de la couche Application

|Interfaces utilisateur et services de réseau| La couche Application fournit des interfaces permettant aux utilisateurs ou aux applications d'accéder aux services du réseau. Par exemple, lorsqu'un utilisateur consulte une page web via un navigateur, la couche Application fournit l’interface qui permet à cette interaction d'avoir lieu.|
|Accès aux services réseau| Elle permet à des applications de demander des services réseau comme l'envoi d'un fichier, la navigation sur le web, ou l'envoi d'un e-mail. Elle interprète les requêtes des applications et les traduit en opérations réseau, en s'appuyant sur les couches inférieures pour la transmission des données.| 
|Gestion des transactions|Dans les systèmes distribués ou les bases de données en réseau, la couche Application peut gérer les transactions et coordonner l'accès à des ressources partagées, garantissant que les actions sont bien effectuées de manière ordonnée.|
|Gestion de la synchronisation et du contrôle de données|Elle peut également inclure des mécanismes de contrôle et de synchronisation des données, notamment dans les échanges complexes de type client-serveur.|
|Support de différents protocoles d'application|Cette couche implémente et prend en charge divers protocoles de communication réseau dédiés à des applications spécifiques.|


### Exemples de protocoles à la couche Application

|HTTP (Hypertext Transfer Protocol)| FTP (File Transfer Protocol)|SMTP (Simple Mail Transfer Protocol)|DNS (Domain Name System)|POP3/IMAP|Telnet/SSH|
|-----|------|
|Utilisé pour le transfert de pages web. C’est le protocole sur lequel repose la navigation web.|Utilisé pour transférer des fichiers entre des systèmes via un réseau.|Protocole utilisé pour l'envoi d’e-mails.|Utilisé pour la résolution de noms de domaine en adresses IP.|Protocoles pour récupérer des e-mails depuis un serveur.|Utilisés pour établir des connexions distantes à un ordinateur et exécuter des commandes à distance.|





## 3 - comment utiliser OSI ?


### 1 - L’approche down/top





### 2 - L’approche top/down



### 3 - L’approche divide and conquer







