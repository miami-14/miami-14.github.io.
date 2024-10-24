## Informations 

- [Le modèle OSI](#Le-modèle-OSI)
   - [1- Les origines du modèle OSI](#1-Les-origines-du-modèle-OSI)
   - [2-OSI vue d’ensemble](#2-OSI-vue-d-ensemble)
   - [3-comment utiliser OSI ?](#3-comment-utiliser-OSI)


- [Le modèle TCP/IP](#Le-modèle-TCP/IP)
   - [1-L’IETF](#1-L-IETF)
   - [2-Les-couches-du-modèle-TCP-IP](#2-Les-couches-du-modèle-TCP-IP)

-[L’encapsulation et la décapsulation](#L-encapsulation-et-la-décapsulation).

      
# Le modèle OSI


## 1-Les origines du modèle OSI

`Le modèle OSI` (****Open Systems Interconnection****), proposé par l'ISO (****International Organization for Standardization****) en 1984, est un modèle de référence à sept couches conçu pour structurer l'interconnexion de systèmes ouverts. Bien que les protocoles spécifiques de l'OSI soient aujourd'hui considérés comme obsolètes, notamment avec la prépondérance d'Ethernet et IP, ce modèle reste un cadre de référence fondamental pour de nombreux standards et un langage commun pour les professionnels du réseau.


`Le modèle OSI` ne cherche pas à spécifier des technologies ou des moyens d'interconnexion particuliers, mais vise à décrire `les principes de communication externe entre systèmes`. Un système est dit "ouvert" s'il respecte ces principes dans ses échanges. L’objectif principal du modèle est d'offrir une base commune permettant de coordonner l'élaboration des normes d'interconnexion de systèmes et de positionner les normes existantes dans ce cadre.



Il est important de noter que le modèle OSI n'est pas conçu pour être une spécification technique ou une base d'évaluation des implémentations réelles. Il s'agit plutôt d'un cadre conceptuel permettant aux équipes d’experts de travailler sur des normes indépendamment pour chaque couche, favorisant ainsi une approche productive et standardisée du développement des systèmes d'interconnexion.


## 2-OSI vue d ensemble

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
 


| ****Nom**** | ****Son rôle**** | 
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
 

| ****Nom**** | ****Son rôle****| 
|-----|---------| 
| Encadrement (framing| La couche Liaison segmente les données en blocs appelés trames (ou frames) avant leur envoi. Chaque trame contient les données à transmettre ainsi que des informations de contrôle pour permettre la gestion et la vérification de la transmission.| 
|Adressage physique (MAC)|  Elle assure l'identification des dispositifs sur le réseau à l'aide des adresses physiques MAC (Media Access Control). Chaque appareil sur un réseau possède une adresse MAC unique qui permet de les identifier à ce niveau.| 
|Détection et correction d'erreurs|  La couche Liaison de données intègre des mécanismes pour détecter les erreurs de transmission, tels que les bits de contrôle (CRC – Cyclic Redundancy Check), et, dans certains cas, corriger ces erreurs avant que les données ne soient envoyées à la couche supérieure.|
|Contrôle de flux| Elle régule le flux des données entre deux appareils pour éviter qu’un récepteur soit submergé par trop de données à la fois.| 
| Accès au support (MAC) |  Elle définit des règles pour décider quand et comment les dispositifs peuvent accéder au médium de transmission. Par exemple, dans un réseau Ethernet, le protocole CSMA/CD (Carrier Sense Multiple Access with Collision Detection) est utilisé pour éviter les collisions lors de la transmission de données.|
| Fiabilité de la transmission| La couche Liaison garantit que les données arrivent correctement et dans l’ordre. Si des erreurs sont détectées dans une trame, elle peut demander la retransmission de la trame concernée.| 



### Sous-couches de la couche Liaison de données est divisé en deux :

|****Sous-couche LLC (Logical Link Control)**** | ****Sous-couche MAC (Media Access Control)****|
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

| ****Nom**** | ****Son rôle****| 
|-----|-------| 
|Routage | La fonction la plus importante de cette couche est de déterminer le meilleur chemin pour transmettre les paquets de données d'un nœud à un autre. Cela inclut la gestion des routes entre les réseaux locaux et distants, en utilisant des algorithmes de routage (ex: OSPF, BGP, RIP).| 
|Adressage logique (IP)|  Contrairement à la couche Liaison qui utilise des adresses MAC, la couche Réseau utilise des adresses IP (Internet Protocol) pour identifier de manière unique chaque dispositif sur un réseau global, ce qui permet la communication au-delà des réseaux locaux.| 
|Fragmentation et réassemblage des paquets| Si la taille d’un paquet de données dépasse la capacité maximale d'une liaison, la couche Réseau peut le fragmenter en plusieurs morceaux et ensuite les réassembler à destination.| 
|Interconnexion des réseaux |  La couche Réseau permet à différents réseaux de communiquer entre eux en utilisant des routeurs, qui relient des réseaux locaux (LAN) à des réseaux étendus (WAN) ou à l'Internet.|
|Contrôle de congestion| Pour éviter une surcharge du réseau, la couche Réseau peut mettre en œuvre des mécanismes de contrôle de la congestion, en ajustant le flux de données lorsqu’un réseau est saturé.|
|Gestion des erreurs et diagnostics| Cette couche permet également de surveiller le réseau, de détecter les pannes ou les erreurs, et de générer des messages de diagnostic (par exemple, avec le protocole ICMP, utilisé par la commande ping).| 

### Protocoles associés à la couche Réseau :

| ****Nom**** | ****Son rôle**** | 
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

| ****Nom**** | ****Son rôle**** | 
|-----|-------| 
| Segmentation et réassemblage |La couche Transport segmente les données en paquets (ou segments) de taille appropriée pour être envoyés sur le réseau. Ensuite, elle réassemble ces segments une fois arrivés à destination.|
|Contrôle de flux |Elle régule le flux de données pour éviter de surcharger le récepteur en envoyant trop de données à la fois. Le protocole TCP, par exemple, utilise des mécanismes comme le contrôle de congestion. |
| Contrôle d’erreurs |La couche Transport assure que les données sont envoyées sans erreur et dans le bon ordre. Elle effectue la vérification des erreurs et peut demander la retransmission des segments corrompus ou manquants. | 
| Multiplexage et dé-multiplexage | Elle permet à plusieurs applications sur un même hôte d’utiliser le réseau simultanément en distinguant les connexions grâce à des ports. Chaque application utilise un port spécifique pour communiquer via TCP ou UDP.|
| Connexion orientée ou non | Selon le protocole utilisé (par exemple, TCP ou UDP), la couche Transport peut établir une connexion fiable et orientée connexion (comme TCP), ou offrir un service de communication non orienté connexion, moins fiable mais plus rapide (comme UDP).| 


### Les deux principaux protocoles de la couche Transport

| ****TCP (Transmission Control Protocol)**** |****UDP (User Datagram Protocol)****| 
|-----|-------| 
| C'est un protocole orienté connexion qui garantit la livraison des paquets dans l'ordre et sans erreur. Il est utilisé pour des applications nécessitant une grande fiabilité, comme le web (HTTP), le courrier électronique (SMTP), ou le transfert de fichiers (FTP).| C'est un protocole non orienté connexion, plus léger et plus rapide que TCP, mais sans garantie de livraison ou d'ordre. Il est utilisé dans des applications où la vitesse est prioritaire sur la fiabilité, comme la diffusion en continu (streaming), les jeux en ligne ou les appels VoIP.| 

![image](https://github.com/user-attachments/assets/01a36943-0f63-4a76-a5f2-927a2a1e0056)

--------------------
### 5 - La couche Session

`La couche Session` est la cinquième couche du modèle OSI (Open Systems Interconnection) et elle est chargée de gérer les sessions entre les applications qui communiquent sur le réseau. Une "session" est essentiellement une connexion logique établie entre deux dispositifs ou applications pour permettre l'échange de données.

### Les principales fonctions de la couche Session 

|****Nom****|****Son rôle****| 
|----|------|
|Gestion des dialogues (ou dialogues de communication)|  La couche Session organise et synchronise le dialogue entre deux applications. Elle établit, maintient et termine les sessions de communication. Cela signifie qu'elle garantit que les deux parties peuvent échanger des données de manière ordonnée.|
|Contrôle de la synchronisation | Elle permet l'ajout de points de synchronisation (ou de "checkpoints") dans la communication, ce qui facilite la reprise des échanges en cas de panne ou d'interruption. Par exemple, si une session est interrompue, la couche Session peut décider de redémarrer à partir du dernier point de contrôle, plutôt que de recommencer depuis le début.| 
| Ouverture, fermeture et gestion de sessions|La couche Session s’assure que les sessions sont correctement ouvertes et fermées. Elle peut gérer plusieurs sessions actives en même temps et assurer qu'elles fonctionnent correctement sans interférer les unes avec les autres.
| Contrôle du jeton (Token Management)| Dans certaines communications, la couche Session peut gérer un mécanisme de jeton (token), où une seule partie peut envoyer des données à un moment donné, pour éviter des collisions ou des conflits de communication.| 
|Rétablissement après erreur| Si une session est interrompue de façon inattendue, la couche Session peut être responsable de reprendre la communication à partir de là où elle s'était arrêtée.|

### Exemples d’utilisation de la couche Session :

|****Protocole NetBIOS**** |****RPC(Remote Procedure Call)****| 
|-----|------| 
|Ce protocole, utilisé dans des réseaux locaux, fonctionne à la couche Session en permettant à des applications d'établir une session de communication et de s'authentifier.| Les appels de procédure à distance, utilisés pour exécuter des fonctions sur des systèmes distants, s'appuient sur la couche Session pour gérer les connexions.| 

------------------------

### 6 - La couche Présentation

`La couche Présentation` est la sixième couche du modèle OSI (Open Systems Interconnection). Elle est parfois appelée la couche de traduction, car son rôle principal est de s'assurer que les données envoyées par une application sur un réseau peuvent être comprises par l'application réceptrice, même si ces applications utilisent des formats de données différents.

### Les fonctions principales de la couche Présentation

| ****Nom**** | ****Son rôle**** | 
|------|-----| 
| Traduction des formats de données | Les systèmes différents peuvent utiliser des formats de données distincts. La couche Présentation traduit les formats utilisés par les applications en un format standardisé pour que les données puissent être échangées de manière compréhensible. Par exemple, elle peut convertir des données du format ASCII vers EBCDIC. | 
| Cryptage et décryptage | Si des données doivent être échangées de manière sécurisée, la couche Présentation prend en charge le chiffrement avant la transmission et le déchiffrement à la réception. C’est à ce niveau que les algorithmes de cryptage (comme SSL/TLS) sont souvent implémentés. |
| Compression des données | Pour améliorer l'efficacité de la transmission, cette couche peut compresser les données avant qu'elles ne soient envoyées sur le réseau et les décompresser à la réception. Cela permet d'optimiser la bande passante et d'accélérer la transmission. |  
| Gestion des formats multimédia | La couche Présentation s'occupe également de la gestion des formats multimédia, tels que les images, les vidéos et le son. Elle s'assure que les fichiers multimédias envoyés dans un certain format sont correctement interprétés et affichés par la machine réceptrice. |


### Exemples d'utilisation de la couche Présentation :

| ****JPEG, GIF, PNG**** | ****SSL/TLS**** | 
|----|-----| 
| Ces formats de fichiers d'images sont interprétés à la couche Présentation. Les données binaires d’une image sont traduites en données compréhensibles pour les applications. | Les protocoles de sécurisation des communications sur Internet (comme HTTPS) fonctionnent en grande partie à la couche Présentation pour chiffrer et déchiffrer les données échangées entre un client et un serveur. |



-----------------------------

### 7 - La couche Application 

`La couche Application` est la septième et dernière couche du modèle OSI (Open Systems Interconnection). C’est celle qui est la plus proche de l’utilisateur final et des applications réseau. Son rôle principal est de fournir des interfaces et des services pour les applications logicielles qui doivent communiquer à travers le réseau. Contrairement aux couches sous-jacentes, la couche Application ne traite pas directement la transmission des données, mais gère l’interaction entre l’utilisateur et l’application réseau.

### Fonctions principales de la couche Application

| ****Nom**** | ****Son rôle**** | 
|------|-----|
|Interfaces utilisateur et services de réseau| La couche Application fournit des interfaces permettant aux utilisateurs ou aux applications d'accéder aux services du réseau. Par exemple, lorsqu'un utilisateur consulte une page web via un navigateur, la couche Application fournit l’interface qui permet à cette interaction d'avoir lieu.|
|Accès aux services réseau| Elle permet à des applications de demander des services réseau comme l'envoi d'un fichier, la navigation sur le web, ou l'envoi d'un e-mail. Elle interprète les requêtes des applications et les traduit en opérations réseau, en s'appuyant sur les couches inférieures pour la transmission des données.| 
|Gestion des transactions|Dans les systèmes distribués ou les bases de données en réseau, la couche Application peut gérer les transactions et coordonner l'accès à des ressources partagées, garantissant que les actions sont bien effectuées de manière ordonnée.|
|Gestion de la synchronisation et du contrôle de données|Elle peut également inclure des mécanismes de contrôle et de synchronisation des données, notamment dans les échanges complexes de type client-serveur.|
|Support de différents protocoles d'application|Cette couche implémente et prend en charge divers protocoles de communication réseau dédiés à des applications spécifiques.|


### Exemples de protocoles à la couche Application

| ****HTTP (Hypertext Transfer Protocol)**** | ****FTP (File Transfer Protocol)**** | ****SMTP (Simple Mail Transfer Protocol)**** | ****DNS (Domain Name System)**** | ****POP3/IMAP**** | ****Telnet/SSH**** |
|-----|------|------|------|------|------|
| Utilisé pour le transfert de pages web. C’est le protocole sur lequel repose la navigation web. | Utilisé pour transférer des fichiers entre des systèmes via un réseau. | Protocole utilisé pour l'envoi d’e-mails. | Utilisé pour la résolution de noms de domaine en adresses IP. | Protocoles pour récupérer des e-mails depuis un serveur. | Utilisés pour établir des connexions distantes à un ordinateur et exécuter des commandes à distance. |



------------------------


## 3-comment utiliser OSI


`Le modèle OSI` (****Open Systems Interconnection****) est principalement un cadre conceptuel utilisé pour comprendre comment les différents protocoles de communication interagissent dans un réseau informatique. Bien que le modèle OSI ne soit pas utilisé directement dans la configuration des réseaux, il fournit une base théorique pour organiser et décomposer les processus de communication en couches distinctes. En pratique, ce modèle est surtout utile pour diagnostiquer, analyser, et concevoir des systèmes et des protocoles réseaux.


### 1 - L’approche down/top

L'approche Top-down, ou descendante, consiste à aborder un système en commençant par les niveaux les plus élevés de sa structure, en le décomposant progressivement en sous-systèmes et en composants de plus en plus détaillés. Cette méthode va du plus général au plus spécifique.

### Caractéristiques

|****Nom****|****Son role****|
|----|-----|
|Décomposition hiérarchique|On commence par un objectif global ou une vue d'ensemble, puis on divise le système en sous-parties plus petites et plus gérables.|
|Abstraction élevée au départ| La conception globale du système est la première étape, puis les détails sont raffinés au fur et à mesure.|
|Contrôle centralisé| Souvent utilisée dans des environnements où la gestion centrale est nécessaire. Les décisions stratégiques sont prises au sommet, puis transmises vers les niveaux inférieurs pour être exécutées.|
|Clarté des objectifs|Avant de s'attaquer aux détails, les objectifs globaux du projet sont définis.|


### Exemple d'utilisation 

| ****Développement logiciel**** | ****Réseaux informatiques**** |
|-----|-----| 
| Dans un projet de développement, l'architecture générale du système est définie avant d’entrer dans le détail des modules spécifiques ou des fonctions individuelles. Par exemple, on commence par concevoir le framework global d'une application avant de développer les modules spécifiques. | Lors de la conception d'un réseau, on peut commencer par une vision d'ensemble du réseau (comme un plan pour une infrastructure de campus) puis subdiviser le réseau en sous-réseaux, choisir les équipements de réseau, configurer les routeurs, commutateurs, etc. |



### Avantages 

-Offre une vue d'ensemble claire du système.

-Réduit les risques d'erreurs majeures en se concentrant sur la structure avant les détails.

-Facilite la planification à long terme, car le but global est toujours en vue.


### Inconvénients

- Peut être moins flexible dans un environnement où les besoins évoluent fréquemment.

- Nécessite une vision claire dès le départ, ce qui peut être difficile dans des systèmes complexes et incertains.


-----------------


### 2 - L’approche top/down

L'approche top-down (ou descendante) est une méthodologie qui consiste à analyser, concevoir ou résoudre un problème en commençant par les concepts les plus généraux pour aller progressivement vers des détails plus spécifiques. Elle est utilisée dans de nombreux domaines, tels que l'ingénierie, le développement logiciel, la gestion de projets, et même la gestion d'entreprises. Cette approche commence par une vision globale ou un objectif final, et divise ensuite ce grand ensemble en sous-parties gérables jusqu'à arriver aux composants individuels ou aux tâches spécifiques.



### Caractéristiques de l’approche top-down

| ****Nom**** | ****Son rôle**** | 
|----|-----| 
| Définition d’un objectif global | Le processus commence par une vue d’ensemble du système ou du problème à résoudre. Il est essentiel d’avoir une idée claire de l’objectif final avant de commencer la décomposition. |
| Décomposition hiérarchique | Le système ou problème est décomposé en sous-systèmes ou sous-problèmes. Ces parties sont ensuite subdivisées jusqu’à atteindre un niveau de détail qui permet de les aborder individuellement. |
| Planification structurée | Cette approche permet de garder une vision d'ensemble tout au long du processus, ce qui facilite la coordination et la planification des étapes. |
| Focus sur la coordination | Comme la décomposition vient de la vision globale, les sous-parties sont étroitement liées à l’objectif final, ce qui réduit le risque que des sous-parties développées indépendamment manquent de cohérence. |



### Exemple d'utilisation dans divers domaines 


| ****Développement logiciel**** | ****Conception de réseau**** | ****Gestion de projets**** | ****Stratégie d'entreprise**** |
|----|----|----|----|
| Dans le développement logiciel, une approche top-down consiste à concevoir d'abord l'architecture globale du programme ou du système. Par exemple, on peut commencer par définir que le logiciel aura une interface utilisateur, une base de données, et des services d’arrière-plan. Ensuite, chaque composant est développé de manière plus détaillée (création des interfaces, gestion des données, etc.). | Lors de la conception d’un réseau, l’approche top-down commence par définir l’architecture globale du réseau (nombre de sites, types de connexion, niveaux de sécurité, etc.). Ensuite, on décompose chaque segment du réseau en fonction des exigences spécifiques (LAN, WAN, configurations des routeurs et switches, etc.). | Dans la gestion de projets, l’approche top-down implique de commencer par les objectifs globaux du projet et de les diviser en phases ou étapes, puis en sous-tâches plus spécifiques. Par exemple, dans un projet de construction, vous commencez par planifier les grandes étapes (design, construction, finalisation), puis vous subdivisez chaque étape en tâches spécifiques comme l’achat des matériaux, la gestion du personnel, etc. | Dans une entreprise, une approche top-down pourrait être utilisée pour fixer des objectifs stratégiques globaux (par exemple, augmenter les revenus de 20 % sur 5 ans), puis diviser cet objectif en sous-objectifs pour chaque département (marketing, ventes, développement produit, etc.). Chaque département fixe ensuite ses propres objectifs basés sur l’objectif global de l’entreprise. |




### Avantages de l'approche top-down

- Clarté d’ensemble : L’approche permet d’avoir une vue d’ensemble du projet, du système ou du problème dès le départ, ce qui aide à mieux coordonner les efforts et à s'assurer que toutes les sous-parties contribuent à l'objectif global.

- Organisation et planification : Elle permet de structurer le projet de manière hiérarchique, facilitant la gestion et la planification des tâches.

- Meilleure coordination : En partant de la vision globale, toutes les sous-parties sont alignées sur le même objectif, ce qui facilite leur intégration au fur et à mesure.

- Risque réduit de redondance : Comme la décomposition est planifiée à partir d'une vision centralisée, cela minimise les doublons ou les conflits dans la conception.


### Inconvénients de l'approche top-down :

- Moins flexible : Si les exigences changent au cours du projet, il peut être difficile d'ajuster la conception globale une fois que la décomposition est avancée.

- Complexité initiale : La planification détaillée de l’ensemble du système dès le début peut être difficile dans des projets très complexes ou incertains, où tous les détails ne sont pas connus d'avance.

-Dépendance aux décisions initiales : Si la structure ou l'architecture globale est mal définie dès le départ, cela peut entraîner des problèmes dans les étapes suivantes et être difficile à corriger en cours de route.


------------------

### 3 - L’approche divide and conquer

L'approche "Divide and Conquer" (ou "Diviser pour régner") est une méthode algorithmique et de résolution de problèmes qui consiste à décomposer un problème complexe en sous-problèmes plus simples, à résoudre ces sous-problèmes individuellement, puis à combiner leurs solutions pour obtenir la solution globale du problème initial. Cette approche est utilisée dans divers domaines, notamment en informatique, en mathématiques, en gestion, et même dans la stratégie militaire.


### Principe de l'approche "Divide and Conquer"

| ****Nom**** |****Son rôle****|
|----|----|
|Division| Le problème global est divisé en plusieurs sous-problèmes plus petits et similaires au problème initial, mais plus faciles à résoudre.|
|Conquête (Résolution)|Chaque sous-problème est résolu indépendamment. Si un sous-problème est suffisamment simple, il est résolu directement. Sinon, il est encore subdivisé.|
|Combinaison | Les solutions des sous-problèmes sont ensuite combinées pour former la solution finale du problème initial.|

### Exemples d'utilisation de l'approche "Divide and Conquer"

| ****Tri rapide (Quicksort)**** | ****Tri fusion (Mergesort)**** | ****Algorithme de recherche binaire**** |
|----|----|----|
| Un exemple classique. Pour trier une liste, on choisit un élément pivot, on divise la liste en deux sous-listes (les éléments inférieurs au pivot et les éléments supérieurs), on trie récursivement les sous-listes, puis on les combine. | L'algorithme divise un tableau en deux moitiés, trie chaque moitié de manière récursive, puis fusionne les deux moitiés triées pour former le tableau trié complet. | Dans un tableau trié, on divise l'espace de recherche en deux à chaque étape, en comparant l'élément central avec l'élément recherché, puis on continue dans la moitié qui peut contenir l'élément cible. |


### Avantages de l'approche "Divide and Conquer"

- `Simplicité` : En décomposant un problème complexe en parties plus petites et plus faciles à résoudre, cette méthode permet de simplifier le processus de résolution.

- `Efficacité` : Les sous-problèmes peuvent souvent être résolus plus rapidement que le problème global, ce qui permet d’optimiser les calculs ou le processus de résolution.

- `Récursivité` : Cette approche est souvent implémentée de manière récursive, ce qui permet de réduire la complexité du code et de le rendre plus modulaire.

- `Répartition des tâches` : Dans la gestion de projets ou d’équipes, cette approche permet de répartir les tâches entre plusieurs équipes ou personnes, ce qui accélère le travail global.


### Inconvénients de l'approche "Divide and Conquer"

- `Complexité de la combinaison` : Si les sous-problèmes sont simples à résoudre, la phase de combinaison des solutions peut parfois être plus complexe que la résolution des sous-problèmes eux-mêmes.

- `Répétition des calculs` : Dans certains cas, des sous-problèmes peuvent se chevaucher, entraînant la répétition inutile de calculs. Cela peut être atténué par des techniques comme la mémoïsation (mémorisation des résultats déjà calculés).

- `Récursivité coûteuse` : L’utilisation de la récursivité peut parfois entraîner une surcharge en termes de mémoire ou de temps d’exécution si le nombre de sous-problèmes est trop élevé. Il est parfois nécessaire de transformer la récursivité en une approche itérative pour optimiser l’algorithme.





# Le modèle TCP/IP
`Le modèle TCP/IP` (****Transmission Control Protocol/Internet Protocol****) est un ensemble de protocoles de communication utilisés pour interconnecter des dispositifs en réseau, notamment sur Internet. Il définit comment les données doivent être formatées, transmises, acheminées et reçues à destination. Le modèle TCP/IP est structuré en quatre couches, chacune ayant des responsabilités spécifiques pour gérer différents aspects des communications réseau.


## 1-L IETF
L'IETF (Internet Engineering Task Force) est une organisation ouverte et internationale qui développe et promeut des normes pour assurer le bon fonctionnement et l'évolution de l'Internet. Fondée en 1986, l'IETF est à l'origine de la plupart des protocoles qui régissent le fonctionnement de l'Internet, y compris des protocoles fondamentaux comme TCP/IP, HTTP, SMTP et DNS.
 


### 1. La hiérarchie

IESG (Internet Engineering Steering Group)


|****Rôle ****|****Composition**** |****Responsabilités**** | 
|---|---|---|
|Le groupe de direction de l'ingénierie Internet (IESG) est chargé de la supervision technique et du contrôle de la qualité des processus de normalisation. Il joue un rôle clé dans la validation des normes Internet et approuve les documents (tels que les RFC) proposés par les groupes de travail de l'IETF.|L'IESG est composé de directeurs de zone, chacun étant responsable d'un domaine technique spécifique (par exemple, routage, sécurité, transport, etc.). Ces directeurs sont élus parmi la communauté de l'IETF.|En plus d'approuver les documents produits par les groupes de travail, l'IESG s'assure que les travaux avancent de manière cohérente et que les nouvelles normes répondent aux exigences techniques.| 


IAB (Internet Architecture Board)

|****Rôle****|****Composition****|****Responsabilités****| 
|---|---|---|
| Le Conseil d'architecture de l'Internet (IAB) est responsable de la supervision globale de l'architecture de l'Internet et de la gestion technique de l'IETF. Il agit comme un organe consultatif et de supervision stratégique, assurant que les décisions prises à court terme s'alignent avec la vision à long terme de l'Internet. | L'IAB est composé de membres nommés, qui sont des experts techniques et des personnalités influentes de la communauté Internet. | - Superviser l'évolution de l'architecture Internet. <br> - Nommer les membres de l'IESG. <br> - Examiner et approuver certaines décisions critiques, comme la création ou la suppression de groupes de travail. |

Groupes de travail (Working Groups)

|****Rôle****|****Composition****|****Responsabilités****| 
|---|---|---|
|Les groupes de travail sont le cœur de l'IETF et sont chargés de la production des spécifications techniques, telles que les RFC (Request for Comments). Chaque groupe de travail est spécialisé dans un domaine ou un protocole spécifique et travaille de manière collaborative pour résoudre des problèmes techniques, développer de nouveaux standards ou améliorer des protocoles existants.|Les groupes de travail sont ouverts à toute personne intéressée par les sujets traités. Ils sont coordonnés par un ou plusieurs présidents de groupe de travail (chairs), qui sont nommés par l'IESG et assurent la gestion des discussions et de l'avancement des travaux.|Les décisions sont prises par consensus, et les discussions se déroulent principalement par le biais de listes de diffusion, bien que des réunions physiques aient lieu lors des événements IETF.|


NomCom (Nominations Committee)

|****Rôle****|****Composition****|****Fonctionnement****| 
|---|---|---|
|Le Comité de nomination (NomCom) est chargé de sélectionner les membres de l'IAB et de l'IESG. C'est un organe indépendant qui assure que les personnes sélectionnées pour ces rôles sont compétentes et respectées au sein de la communauté IETF.| Le NomCom est composé de membres tirés au sort parmi les participants actifs de l'IETF, pour garantir une certaine impartialité et représentativité.|Le processus de nomination est généralement basé sur la transparence, et les membres du NomCom consultent la communauté pour recueillir des retours sur les candidats avant de prendre une décision finale.|

Internet Society (ISOC)

|****Rôle****|****Relation avec l'IETF****|
|---|---|
|L'Internet Society (ISOC) est l'organisation mère qui soutient l'IETF sur le plan logistique et financier. L'ISOC ne joue pas un rôle direct dans les décisions techniques, mais elle fournit l'infrastructure nécessaire pour que l'IETF puisse fonctionner. Elle est également responsable de la promotion d'un Internet ouvert et accessible pour tous.|L'ISOC gère les aspects financiers, juridiques et administratifs de l'IETF, mais elle reste en dehors des processus techniques et des décisions liées aux protocoles.|

RFC Editor

|****Rôle****|****Fonctionnement****| 
|---|---|
| Le RFC Editor est responsable de la publication des RFC (Request for Comments), les documents techniques produits par l'IETF. Ce rôle est crucial pour s'assurer que les spécifications sont publiées de manière claire, standardisée et accessible à tous.|Bien que le contenu technique des RFC soit validé par l'IETF, l'éditeur de RFC garantit la cohérence et la qualité rédactionnelle de ces documents.|

IAOC et IETF Trust

|****Rôle****|
|---|
|Le Comité de supervision des affaires de l'IETF (IAOC) et le IETF Trust sont des entités responsables de la gestion des aspects financiers et juridiques. L'IAOC gère les contrats, les services, et veille à ce que l'IETF dispose des ressources nécessaires pour fonctionner. Le IETF Trust détient les droits de propriété intellectuelle et les marques associées à l'IETF, garantissant que les documents et protocoles développés restent accessibles à tous.|

![image](https://github.com/user-attachments/assets/1ed4fe94-ef10-4009-b6ec-a0fcc196d594)

-------------------
### 2. Les RFC
Les RFC (Request for Comments) sont des documents techniques et de recherche utilisés pour décrire les normes, les protocoles, et les technologies liés à l'Internet. Créés par des experts et des ingénieurs, ils constituent une base fondamentale pour le développement et la gestion de l'Internet.

Fonctionnement :

|****Nom****|****rôle****|
|---|---|
|Proposition|Les RFC sont généralement rédigées par des membres de la communauté Internet, souvent dans le cadre de l'IETF (Internet Engineering Task Force). Les documents passent par plusieurs étapes de révision et de validation avant d’être acceptés comme standard.|
|Numérotation|Chaque RFC reçoit un numéro unique et est disponible publiquement. Par exemple, RFC 791 décrit IPv4.|


Catégories de RFC : 

|****Nom****|****rôle****|
|---|---|
|Standards Track|Documents définissant des normes officielles comme les protocoles de base de l'Internet.|
|Informational |Informations générales ou des descriptions techniques sans qu'elles ne soient des standards officiels.|
|Experimental|Propositions de technologies en phase d’expérimentation, non encore approuvées comme standard.|
|Best Current Practice (BCP)|Des recommandations pratiques pour les opérations de l'Internet.|




## 2-Les couches du modèle TCP IP
Cours sur Couche 2

<a href="https://github.com/miami-14/miami-14.github.io./tree/main/SISR/Couche%202" target="_blank">Cours Couche 2 </a>

![image](https://github.com/user-attachments/assets/b3f44e65-e33b-4eef-86b7-2e9f2c88bc38)


### 1. La couche Accès réseau

`La couche d'accès réseau` fait partie du modèle OSI (Open Systems Interconnection) qui assure la transmission des données physiques sur le réseau. Elle définit comment les données sont physiquement envoyées à travers les supports (câbles, ondes radio, etc.). Cette couche s'occupe des interfaces matérielles, des méthodes de modulation, de la gestion des connexions et des protocoles d'accès au support, comme Ethernet ou Wi-Fi. Elle assure que les bits sont transmis correctement d'un appareil à un autre.

-------------------
### 2. La couche Internet

`La couche Internet` (ou couche réseau) est une partie du modèle TCP/IP. Elle gère le routage des paquets de données à travers différents réseaux jusqu'à leur destination. Cette couche utilise principalement le protocole IP (Internet Protocol) pour définir l'adresse des hôtes et déterminer le meilleur chemin à suivre pour les données. Elle s'occupe aussi de la fragmentation des paquets en cas de besoin. Elle joue un rôle crucial dans la communication entre différents réseaux, comme Internet.

- Les protocoles principaux incluent l'IP, ICMP, et ARP.

![Capture d'écran 2024-10-20 180153](https://github.com/user-attachments/assets/c1e8bcbe-a0dd-4ae7-8c34-e8ebcbb0e159)

------------------
### 3. La couche Transport

`La couche Transport` du modèle TCP/IP garantit la livraison fiable des données entre deux systèmes. Elle gère la segmentation des données, le contrôle de flux, et la détection d'erreurs. Deux protocoles principaux opèrent à ce niveau :

- TCP (Transmission Control Protocol) : fournit une connexion fiable et garantit que les données arrivent dans le bon ordre et sans perte.

- UDP (User Datagram Protocol) : plus léger, il n'assure pas la fiabilité ni l'ordre des paquets, mais est plus rapide pour des applications comme le streaming.

Elle s'assure que les données sont envoyées et reçues correctement entre les applications.

------------------
### 4. La couche Application

`La couche Application` est la couche la plus élevée du modèle TCP/IP et est responsable de l'interaction directe avec les applications et les utilisateurs. Elle fournit les protocoles nécessaires pour les services de réseau comme le web, le courrier électronique et le transfert de fichiers.

Les principaux protocoles incluent

|Nom|Rôle|
|---|---|
|HTTP (pour le web)|HTTP est un protocole de communication client­serveur permettant les échanges destinés au WWW (World Wide Web : littéralement la toile [d’araignée] mondiale) également appelé Web. La plupart du temps, l’application qui utilise ce protocole est le navigateur Internet mais d’autres applications peuvent très bien l’utiliser.|
|HTTPS (pour le web)|HTTPS est la version sécurisée de HTTP et s’appuie pour ce faire sur les protocoles SSL ou TLS. SSL (Secure Socket Layer) est un protocole de sécurisation des échanges développé par Netscape. TLS (Transport Layer Security) en est la version normalisée par l’IETF. Outre la confidentialité des données, SSL ou TLS doivent permettre l’authentification du serveur. Pour mémoire, l’identification répond à la question « Qui es­tu ? », l’authentification répond à la question « Est­ce bien lui ? ».|
|SMTP (pour l'email)|Littéralement, protocole simple de transfert de courrier. L’objet de ce protocole est l’envoi de courrier électronique vers les serveurs de messagerie électronique. Une session SMTP spécifie dans l’ordre l’expéditeur, le destinataire puis le corps du message.|
|FTP (pour le transfert de fichiers)| L’objet de FTP est l’échange de fichiers entre ordinateurs du réseau. FTP fonctionne en mode client­serveur, le serveur répond aux requêtes du client.|
|TELNET|Teletype fait référence au téléscripteur, appareil permettant l’émission et la réception de messages transportés par les lignes filaires du réseau international Télex. L’acronyme universellement accepté de teletype est TTY. C’est le photocopieur qui a fait tomber en désuétude le téléscripteur et donc le réseau Télex. Le protocole TELNET reproduit la fonction du téléscripteur, à savoir le transport de messages sous leur forme basique de caractères, au travers du réseau TCP/IP. TELNET fonctionne également en mode client­serveur. L’acronyme désignant une session TELNET est VTY (Virtual Teletype).|
|POP|Littéralement, protocole du bureau de poste. SMTP ne permet pas de récupérer un message déposé dans la boîte aux lettres d’un serveur de messagerie. Cette fonction est prise en charge par le protocole POP qui en est à sa version 3.|
|DNS|Littéralement système de noms de domaine. DNS a pour objet d’associer un nom intelligible et donc mémorisable par les hommes, à une adresse IP qui, elle, n’est mémorisable facilement que par les machines. L’activité correspondante est appelée résolution de nom de domaine. Résoudre un nom de domaine tel www.eni.fr, c’est trouver l’adresse IP qui lui est associée.|
|TFTP|Littéralement, protocole simplifié de transfert de fichiers. TFTP s’appuie sur UDP, protocole de transport « non fiable ». Les fonctionnalités dont ne dispose pas TFTP par rapport à FTP en rétrécissent l’usage à la mise à jour de logiciels embarqués sur les matériels réseau (routeurs, commutateurs...).|


Cette couche permet aux applications d'interagir avec les autres couches sous-jacentes afin de faciliter la communication entre les appareils sur un réseau.




# L encapsulation et la décapsulation


L'encapsulation et la décapsulation sont des processus fondamentaux dans les communications en réseau.

|Encapsulation |Décapsulation|
|---|---|
|Chaque couche du modèle TCP/IP ajoute des informations spécifiques sous forme d'en-têtes (ou de trailers) aux données avant de les transmettre à la couche suivante. Ce processus enrobe les données dans un format compréhensible pour chaque couche (exemple : application → transport → réseau → accès réseau).|À la réception, les couches du modèle retirent progressivement ces en-têtes (processus inverse de l'encapsulation) pour extraire les données originales.|

Cela garantit une transmission correcte des données entre l'émetteur et le récepteur.

![image](https://github.com/user-attachments/assets/e9ab53d5-a123-47ec-a540-0ad6bb93bfc4)

