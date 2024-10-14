# Couche 2 



## Informations 

- [La couche Liaison de données et ses sous­couches](#La-couche-Liaison-de-données-et-ses-sous­couches)
- [Protiocole](#Protiocole)
- [L’adressage Ethernet](#L-adressage-Ethernet)
- [Dissection d une trame Ethernet](#Dissection-d-une-trame-Ethernet)








# La couche Liaison de données et ses sous­couches


## 1-  Rôle de la couche Liaison de données

La couche Physique fournit aux applications et protocoles des couches supérieures les moyens d’envoyer et de
contrôler les données sur le support physique de transmission.

En plus de contrôler comment les données accèdent au média physique, cette couche fournit un service de détection
d’erreur.

⚠️ qu’il s’agit de détection d’erreur et non de correction d’erreur.


Les protocoles de couche 2 doivent ajouter de l’information à celle déjà existante pour former
un ensemble qu’on appelle une trame.

La couche Liaison de données à `deux sous­couches` :

* `La couche LLC` , IEEE 802.2.
* `La couche MAC`  Il y a plusieurs instances existent :


         * `IEEE 802.3`  (la dénomination d’Ethernet).
         * `IEEE 802.5`  (Token Ring, obsolète aujourd’hui).
         * `IEEE 802.11`  définit les spécifications pour la transmission sans fil (Wi­Fi).


il existe des instances, certaines sont toujours utilisées tandis que d’autres sont frappés petit à
petit d’obsolescence. Actuellement, le protocole prédominant en filaire sur la couche 2 est Ethernet.

Il y a d'autre protocoles, plus ou moins utilisés aujourd’hui, existent sur cette couche. Parmi les protocoles qui sont moins utiliser sont
`IEEE 802.11 Wi­Fi`, `Frame Relay` et `ATM`.


> [!NOTE]
        - La couche LLC=> Logical Link Control

 - La couche MAC=> Media Access Control


## 2- Mac 

Quand un navigateur demande une page Internet, la requête formulée risque très certainement de traverser
différents médias.

La manière dont ces différents médias fonctionnent peut être différente (synchrone, asynchrone, média partagé...)
et utiliser différents formats pour l’adressage des équipements connectés.

> [!NOTE]
         Si il y a pas la couche MAC, les protocoles de niveaux supérieurs devraient gérer chacun de ces médias en s’adaptant aux
         différentes règles qui les régissent.

Grâce à la couche MAC , un équipement donné peut lire les informations contenues dans la
trame entrante, la décapsuler (séparer les données utiles au média des autres) puis la réencapsuler (ajouter les
données nécessaires au média aux données que l’on veut transmettre), sous un nouveau format qui respecte les
méthodes d’accès au nouveau média.

> [!NOTE]
          La  méthode d’accès définit comment un nœud accède et communique au travers d’un média.
         normes IEEE 802.11 Wi­Fi, Frame Relay et ATM.

         Pour décrire de manière plus détaillée ce que nous entendons par règle d’accès au média, par
         exemple dans le cadre d’une conversation.

Lorsqu’une personne souhaite parler dans un groupe, elle attend poliment que la communication en cours soit
terminée. Cette méthode naturelle, appelée communication à "bâtons rompus", peut fonctionner à condition que
chacun y mette de la courtoisie, que personne ne monopolise le temps de parole et que le groupe ne soit pas trop
nombreux.


-
         Par exemple si deux personnes désirent délivrer un message et attendent qu’une troisième termine de délivrer le sien,
         il faut espérer qu’aléatoirement, l’une des deux personnes démarre avant l’autre et occupe ainsi le canal. Si deux
         personnes démarrent simultanément une conversation, les informations vont se télescoper (en informatique on
         parle de collision). Dans ce cas, le réflexe normal est que les deux personnes se taisent, se regardent et espèrent
         qu’à la prochaine tentative, l’une des deux démarrera avant l’autre (sauf si une troisième personne en profite pour
         délivrer son message).

Il existe des méthodes plus rigoureuses comme le "tour de table". La personne qui désire s’exprimer attend son
tour (droit à la parole, micro...). La personne qui obtient son tour n’a pas obligatoirement quelque chose à dire et
dans ce cas transmet le droit de parole à la personne suivante. Ce n’est pas très spontané mais c’est efficace. Il n’y
a pas de risque de collision et un temps de parole est garanti pour chaque interlocuteur.

Historiquement, Ethernet est le protocole qui utilise le mode de communication à "bâtons rompus", ce mode est
aussi appelé "Shared Access Media" ou encore "Contention­Based Access". Deux protocoles ont été développés
pour permettre aux réseaux de fonctionner sur ce modèle, il s’agit de CSMA/CA  pour les liaisons filaires et CSMA/CA 
les connexions sans fil. Ces deux protocoles seront expliqués à la section Le fonctionnement d’Ethernet de ce
chapitre.

* `Token Ring` est le protocole qui utilisait le mode de communication par jeton, analogue au principe de tour de table.
Même si Token Ring est considéré comme obsolète aujourd’hui, son principe de régulation d’accès au média reste
toujours valable.

> [!NOTE]
        - MAC => Media Access Control

  - CSMA/CA => Carrier Sense Multiple Access/Collision Detection


## 3-  LLC
La sous­couche `LLC` sert d’interface pour la couche supérieure, la couche Réseau.

Cette couche permet notamment d’identifier quel protocole de couche supérieure est utilisé, ce qui permet
finalement à plusieurs protocoles différents de couche 3 d’utiliser le même protocole de couche 2.

C’est comme cela que les protocoles IPv4 et IPv6 sont en mesure d’utiliser tous les deux le protocole de couche 2
qui domine l’industrie depuis des années, Ethernet.

Avec Ethernet, la sous­couche LLC identifie le protocole de niveau supérieur en utilisant dans la trame un identifiant
qui est nommé EtherType.

Les valeurs EtherType communes sont :

* l 0x0800 pour IPv4
* l 0x0806 pour ARP
* l 0X86DD pour IPv6
* l 0x891 pour FCoE


La fonction de LLC est très importante car elle permet de fournir un service de multiplexage.

-
         Par exemple un hôte peut avoir activé en même temps plusieurs protocoles de niveau supérieur, la sous­couche LLC
         détermine à partir de l’EtherType à quel processus réseau (network stack) envoyer la trame pour qu’elle soit traitée
         correctement au niveau supérieur. Naturellement, le protocole utilisé sur la couche supérieure est
         totalement transparent pour la sous­couche MAC ou la couche inférieure .

Historiquement, `LLC`pouvait également fournir des services de contrôle de flux et de gestion des
erreurs. Aujourd’hui, la majorité des réseaux utilisent les protocoles de `couche 4 ` pour assurer
les transmissions ce qui ne laisse à `LLC` qu’un rôle de multiplexage.

>[!NOTE]

         - LLC  =>Logical Link Control

        - Couche 4 => la couche Transport
       
        - Couche 1 => La couche Inférieur
       
        - Couche 3 => la couche supérieure

------------------------------------------------------------------------------------------------

# Protiocole 

Ethernet est actuellement le protocole majeur qui règne en maître sur les technologies LAN depuis une dizaine
d’années environ. Depuis sa conception puis sa standardisation, Ethernet n’a fait qu’évoluer et continue d’évoluer au
moment de la rédaction de cet ouvrage.

Ethernet se situe à la fois sur la couche Physique et la couche Liaison de données de la couche OSI. D’un point de vue
du modèle TCP/IP, Ethernet se situe donc sur la couche Accès réseau

![image](https://github.com/user-attachments/assets/02d1d20f-49a6-4c88-bbb3-0517ab0b1c7b)
         
            
                    Sous­couches MAC et LLC

Situé sur ces couches, Ethernet définit à la fois le format des trames, la taille des trames, l’encodage sur le lien
jusqu’aux connecteurs utilisés.

Pour un ingénieur réseau, il est primordial de maîtriser le fonctionnement d’Ethernet car il devra travailler avec lui
pendant encore un très long moment.

------------------------------------------------------------------------------------------------

# L adressage Ethernet

## 1- Le format des adresses

Comme vu précédemment, Ethernet opère à la fois sur la couche Physique et sur la couche Liaison de données de
modèle OSI. Ethernet utilise la sous­couche MAC dont l’une des fonctions est de fournir l’adressage aux
équipements.

Une adresse de couche 2 pour Ethernet qui se nomme une adresse MAC. Elles sont aussi sous le nom
de BIA ou Hardware Addresses. Elles sont assignées par le constructeur directement dans la
carte réseau et on ne peut pas changer l’adresse MAC d’une carte réseau à moins de posséder le matériel
correspond ce qui permettrait de reprogrammer le chipset de ladite carte.

Une adresse MAC a un format précis, elle est composée de 48 bits soit 6 octets et est divisée en deux parties
qui sont dénommées respectivement OUI  et NIC.

>[!IMPORTANT]
L’adresse MAC utilise la représentation hexadécimale, chaque caractère vaut 4 bits.

>[!NOTE]

        - OUI=> Organizationally Unique Identifier

        - NIC=> Network Interface Identifier
        
        - BIA=> Burned In Address

Cette illustration nous montre une adresse MAC et son organisation :


![image](https://github.com/user-attachments/assets/780d2d46-02ad-4203-803f-d51acd21df88)



                              Composition d’une adresse MAC


La partie OUI il y a les trois premiers octets. Dans cette partie, on peut voir comme un préfixe, est assignée
au constructeur par l’IEEE. Pour pouvoir obtenir un préfixe, un constructeur on doit faire la demande et l’acheter
auprès de l’IEEE. Donc on peut dire que tous les constructeurs de cartes réseau Ethernet sont référencés par
l’IEEE.

Un constructeur peut disposer de plusieurs préfixes OUI s’il dépose plusieurs demandes par exemple. 
Cisco figure parmi les premiers constructeurs de la liste avec le préfixe 00­00­0C. Comme vous pourrez le constater,
Cisco possède bien d’autres préfixes OUI.

Il faut garder cette structure de l’adresse MAC à l’esprit si vous trouverez dans des
situations où vous aurez réussi à récupérer l’adresse MAC d’un équipement sans savoir de quel équipement il s’agit.
Utiliser le préfixe OUI permet de récupérer le nom du constructeur et de retrouver l’équipement recherché.
Vous pourrez trouver sur votre moteur de recherche favori une multitude de sites qui proposent de chercher dans la
base IEEE.

NIC est la seconde partie de l’adresse MAC et il y a trois derniers octets. Cette partie est appartient au 
constructeur qui s’engage à n’assigner une adresse qu’une seule fois.

> [!NOTE]
        Il est également intéressant qu’un équipement réseau peut posséder plusieurs adresses MAC.
        Par exemple le cas des switches réseau.

Les adresses MAC peuvent différentes, selon les
constructeurs et les systèmes.

Il y a des systèmes qui utilisent le tiret par exemple  :

* 1C­6F­65­C4­C9­8E

Il y a d'autre utilisent une notation avec un point. Par exemple:

* 1C6F.65C4.C9­8E


##  L’utilisation des adresses

Mais comment sont utilisées ces adresses MAC ?

Quand un équipement émet une trame Ethernet, l’en­tête de niveau 2 possède un certain nombre d’informations.

Avec ces informations Il y a :


- L’adresse MAC source, c’est­à­dire l’adresse MAC de la carte qui émet la trame.
  
- L’adresse MAC de destination, c’est­à­dire l’adresse MAC de la carte qui est censée recevoir la trame.

Bien évidemment, trouver l’adresse MAC source est très simple : une machine connaît sa propre adresse et n’a donc
aucun mal à renseigner ce champ.

L’adresse MAC d’une carte sur un système de type Microsoft
Windows avec la commande `ipconfig /all` sur une invite de commande si dessous 
est un exemple:

Ethernet :

![image](https://github.com/user-attachments/assets/21d3ef80-55ed-45a8-a673-399b2d7c00c9)

![image](https://github.com/user-attachments/assets/68a36d84-fc98-4616-9b0b-958a05a96815)

![image](https://github.com/user-attachments/assets/1ba59011-8050-4c49-a4da-b5c441c2e55a)



Adresse Physique :
![image](https://github.com/user-attachments/assets/865fd442-b3cc-4cbc-b814-9aacfd88f964)

------------------------------------------------------------------------------------------------

# Dissection d une trame Ethernet

## Les composants d’une trame
Pour comprendre le fonctionnement d’Ethernet, il est indipensable de connaître les éléments qui composent une trame Ethernet. La trame la plus rencontré actullement est Ethernet II, car elle est utilisée par les protocoles de niveau supérieur IP.

(image ) 

                        En­tête Ethernet

On peut remarqué, la trame est divisée en plusieurs parties ayant toutes une taille fixe à l’exception du Payload.

Dans le détail, voici les différentes parties de la trame, à l’exception de l’Interpacket Gap qui est la distance entre deux trames en octets :

### - Préambule

Cette information est codée sur 7 octets (56 bits) et est définie sur la couche 1 pour Ethernet.
Les 56 bits sont une suite parfaite de 1 et de 0 dont l’objectif est de signaler une nouvelle trame entrante et de permettre au récepteur de se synchroniser parfaitement avec l’émetteur.


### - SFD (Start Frame Delimiter)

Codée sur 1 octet (8 bits), cette information définie sur la couche 1 pour Ethernet et permet de démarquer la fin du champ Préambule et le début de la trame Ethernet. La valeur des bits du SFD est fixe (10101011).


### - MAC Destination

Après le SFD, les informations définies sur la couche 2 pour Ethernet arrivent. Le champ MAC a une destination qui est simplement l’adresse de niveau 2 de l’interface à qui est destinée la trame et c’est principalement grâce à cette information que les équipements intermédiaires de niveau 2 savent comment switcher la trame 3correctement.


## MAC Source

Le champ MAC Source est l’adresse de niveau 2 de la station qui a émis la trame Ethernet.


### - EtherType

L’EtherType sert à définir quel est le protocole de couche supérieure qui est utilisé. Dans le processus d’encapsulation, l’information a transité par les couches supérieures avant d’arriver sur la couche 2 où est défini l’EtherType. Il est donc possible de savoir quel est le protocole de niveau 3 utilisé.

Voici quelques exemples de valeurs EtherType à retenir :


- 0x0800 indique IPv4.
- l 0x086DD indique IPv6.
- l 0x0806 indique ARP.
- l 0x8906 indique FCoE.


### - Payload

Ce qui est dénommé Payload est à la fois l’information dite "utile" et les en­têtes des couches supérieures.

La longueur est variable, au maximum 1 500 octets. Cette valeur représente la taille maximum d’un paquet qui peut
être transmis sans être fragmenté. Cette valeur est appelée MTU (Maximum Transmission Unit).

### - FCS (Frame Control Sequence)
C’est cette portion d’information qui sert à la détection d’erreur. La station émettrice calcule un chiffre sur 4 octets relatif au contenu de la trame.La station de destination reçoit la trame, elle effectue le même calcul et détermine si le FCS est équivalent. Si le FCS n’est pas le même, cela signifie que la trame est corrompue et elle n’est pas prise en compte.

Il faut ici insister sur le fait qu’il s’agit toujours de détection d’erreur et non de correction d’erreur.


## La taille maximale d’une trame (MTU)

Le champ Payload est décrit comme ayant une valeur de 46 octets (42 octets dans le cas de l’utilisation du protocole 802.1Q) au minimum et 1 500 octets au maximum. Cette valeur est dénommée MTU (Maximum Transmission Unit), donc c'est la taille maximale de données qui peuvent être transportées par Ethernet.


(image) 


Dans certaine situation, les protocoles additionnels viennent ajouter des services complémentaires et ils doivent donc ajouter en en­tête leurs propres informations. Il peut alors être nécessaire de spécifier une valeur MTU plus grande.

On est capable de spécifier une valeur de MTU allant jusqu’à 9 000, on parle alors de Jumbo MTU.


## La trame Unicast

Une trame Unicast est une trame qui est émise par une station et destinée à une seule autre station.

(image ) 


Dans ce type de trame, l’adresse de destination contenue dans le champ MAC Destination est l’adresse d’une station distante, ce qui suppose que la station émettrice soit en possession de cette information.


## La trame Broadcast
Les trames Broadcast sont nécessaires au bon fonctionnement des réseaux locaux actuels.

Pour qu’une trame soit une trame Broadcast, l’adresse contenue dans le champ MAC Destination doit avoir tous les
bits à 1. Cela donne une représentation en FFFF.FFFF.FFFF.

Il est important de savoir que aucune trame ne peut avoir cette adresse Broadcast en tant qu’adresse source. Les
équipements réseau rejettent une trame construite de cette manière.

Cette trame est destinée à toutes les stations :

(image ) 


## La trame Multicast

Une trame Multicast est une trame dont la destination est un groupe de machines. Pour intégré   ce groupe, les machines se sont préalablement enregistrées auprès de ce groupe. Il est donc parfaitement possible d’avoir des groupes de destination Multicast composés de plusieurs dizaines de stations ou bien... d’une seule.

Les trames Multicast a une adresse MAC de destination spéciale dont la plage est 0100.5e00.0000 à 0100.5e7f.ffff. 

Une partie de l’adresse MAC est calculée à partir des 23 bits de l’adresse Multicast de niveau 3.

(image ) 

------------------------------------------------------------------------------------------------

