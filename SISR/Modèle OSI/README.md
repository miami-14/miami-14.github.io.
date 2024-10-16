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

------------------

- Fonctions principales de la couche Liaison de données :
 


| Nom | Son rôle | 
|-----|-----| 
|Transmission de bits|c'est la transmission de bits (0 et 1) entre deux appareils connectés. Ces bits sont transmis sous forme de signaux.|
|Médium de transmission|La couche Physique définit les types de supports physiques utilisés pour la communication ( câble en cuivre, fibre optique, ondes radio )|    
|Caractéristiques des signaux|  Amplitude, fréquence, phase pour les signaux analogiques et Le voltage pour les signaux électriques|
|Topologies physiques|Elle définit la manière dont les dispositifs sont physiquement interconnectés (bus, étoile, anneau, etc.).| 
|Synchronisation des bits|Assure que l’émetteur et le récepteur sont synchronisés pour interpréter les données correctement.|
|Débit de transmission|La couche Physique spécifie la vitesse à laquelle les données peuvent être envoyées (bits par seconde).| 
 

  

### 2 - La couche Liaison de données

La couche Liaison de données est la deuxième couche du modèle OSI. Son rôle principal est d’assurer un transfert de données fiable entre deux nœuds adjacents dans un réseau, en détectant et en corrigeant les erreurs qui pourraient survenir lors de la transmission au niveau de la couche Physique.

-------------------------

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




### 3 - La couche Réseau

La couche Réseau est la troisième couche du modèle OSI, et son rôle principal est de gérer le routage et le transfert des données entre différents réseaux, en assurant que les paquets de données atteignent leur destination finale, même s’ils doivent traverser plusieurs réseaux intermédiaires.

-------------------------

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
|IP (Internet Protocol)| : C'est le protocole fondamental de cette couche, qui se divise en deux versions majeures :IPv4 : La version la plus utilisée, avec des adresses de 32 bits./IPv6 : Une version plus récente, avec des adresses de 128 bits, qui résout le problème de pénurie d'adresses IPv4.  | 
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


### 4 - La couche Transport








### 5 - La couche Session




### 6 - La couche Présentation



### 7 - La couche Application 







## 3 - comment utiliser OSI ?


### 1 - L’approche down/top





### 2 - L’approche top/down



### 3 - L’approche divide and conquer







