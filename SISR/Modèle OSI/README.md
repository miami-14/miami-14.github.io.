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

- Sa fonction: 


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



### 3 - La couche Réseau







### 4 - La couche Transport








### 5 - La couche Session




### 6 - La couche Présentation



### 7 - La couche Application 







## 3 - comment utiliser OSI ?


### 1 - L’approche down/top





### 2 - L’approche top/down



### 3 - L’approche divide and conquer







