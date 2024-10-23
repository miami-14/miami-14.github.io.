# L'adressage Rthernet  


## Information 

[Le format d'une adresse IP4](#Le-format-d-une-adresse-IP4)
[Les classes d adresses IPv4](#Les-classes-d-adresses-IPv4)




# Le format d une adresse IP4

### L’adresse IPv4 et le masque de sous­réseau

Une adresse IPv4 se compose de 32 bits organisés en quatre séquences de 8 bits représentées numériquement et séparées par des points.

Une adresse IPv4 est composée de deux parties que sont :

- L’adresse du réseau (aussi dénommée "préfixe réseau").
- L’adresse de l’hôte.

Pour déterminer quels bits appartiennent à quelle partie, on a recours à un masque de sous­réseau. Le masque, comme l’adresse IPv4, est composé de 32 bits. Une opération AND entre l’adresse IPv4 et le masque permet de déterminer où s’arrête la partie réseau de l’adresse.

Le masque de sous­réseau est donc une suite plus ou moins longue de bits contigus ayant la valeur 1. Cette propriété fait qu’une séquence de 8 bits ne peut avoir qu’une série de valeurs numériques


![image](https://github.com/user-attachments/assets/a62c38a2-2561-492d-9394-c5b796164b6b)

Ces valeurs numériques sont codées sur 8 bits, la longueur totale du masque est donc de 32 bits. Il peut être utile de mémoriser cette séquence par la suite.

Exemple 1 :la division d’une adresse IPv4


![image](https://github.com/user-attachments/assets/355b84cf-5d4e-4785-a58f-438bf2114a08)


En convertissant l’adresse IPv4 et le masque réseau en binaire puis en effectuant une opération AND entre les deux, on obtient un résultat qui correspond à l’adresse réseau.


Dans cet exemple, le masque indique donc que les 16 premiers bits de l’adresse font partie de l’adresse réseau tandis que les 16 derniers bits font partie de l’identification de l’hôte.


![image](https://github.com/user-attachments/assets/231122ef-0b18-4a27-aac9-1eca237c1193)


Le réseau est donc 192.168.0.0. 192.168 fait partie de ce réseau.


- 192.168.1.100
- 192.168.1.0
- 192.168.8.200
- 192.168.14.24

exemple, la démarcation est simple car elle "tombe" entre deux sections de l’adresse. En effet les 2 premiers octets du masque représentent 1 tandis que les 2 derniers octets du masque représentent 0.


Exemple 2 : la démarcation ne tombe pas "juste"

![image](https://github.com/user-attachments/assets/5c14bd78-49d2-4a0e-bd3c-2071fe4aa83a)

le masque n’est plus composé de 16 bits mais de 21 bits. Avec l’opération AND, on constate qu’une machine dont l’adresse est de 192.168.1.1 avec un masque de 255.255.248.0 fait partie du réseau 192.168.0.0.

![image](https://github.com/user-attachments/assets/185442e9-d364-402c-8bda-2c9a7b10ccb8)

il n’y a pas de différence car elle appartient au même réseau.



Exemple 3 : changer l’adresse IPv4 de la machine en conservant le même masque

![image](https://github.com/user-attachments/assets/c7e84a83-82b5-49a3-ab7f-7772e3068c42)

le résultat est différent et il montre qu’une machine avec une adresse IPv4 192.168.128.10 et un masque de 255.255.248.0 fait partie du réseau 192.168.128.0.

Par conséquence, la machine 192.168.128.10 ne fait pas partie du même réseau que la machine 192.168.1.1 lorsque le masque 255.255.248.0 est utilisé


les exemples précédents, le masque a été représenté de manière binaire et de manière numérique.

existe une troisième manière, parfois plus pratique, de représenter le masque aux côtés de l’adresse réseau, cette notation est appelée CIDR

on note par exemple 192.168.128.0/21 pour signifier que le masque contient 21 bits et
que l’adresse réseau est 192.168.128.x. On parle alors aussi de préfixe réseau ou de taille de préfixe.


## La longueur de préfixe et la taille de réseau


La longueur du masque détermine combien de bits sont utilisés pour identifier le réseau et combien sont réservés aux hôtes. Une adresse IPv4 a 32 bits au total. Plus il y a de bits pour la partie réseau, moins il y en a pour les hôtes, ce qui réduit le nombre d’hôtes possibles.

Le nombre d’hôtes dans un réseau se calcule en faisant 2 à la puissance du nombre de bits restants pour la partie hôte.

Exemple 1 : Un masque de 255.255.0.0, ou /16, laisse 16 bits pour les hôtes, soit 2^16 = 65 536 adresses possibles.

Exemple 2 : Un masque de 255.255.248.0, ou /21, laisse 11 bits, donc 2^11 = 2 048 adresses.



Il y a valeurs deux sont réservées: 

- L’adresse dont les bits hôtes valent 0, cette adresse est utilisée pour représenter le réseau.

- L’adresse dont les bits hôtes valent 1, cette adresse est utilisée pour représenter le Broadcast.

Il est important  de retirer deux valeurs pour obtenir le nombre de machines que l’on peut identifier sur un réseau. Pour donner un exemple ci-dessous:

![image](https://github.com/user-attachments/assets/b7097ee5-9724-4cf4-a466-1ebf9b1553f3)

![image](https://github.com/user-attachments/assets/0897bde2-779a-44c4-bfb3-376444a5f4b2)


L’adresse réseau est utilisée pour représenter un réseau, cette adresse est composée  de 0 sur sa partie hôte et elle ne peut pas être attribuée à une interface. En partant sur le diagramme du chapitre La couche Réseau ­ Les fonctions de la couche Réseau, il est possible d’y ajouter les réseaux afin d’avoir une carte de la topologie au niveau IP.

![image](https://github.com/user-attachments/assets/a60215db-5d5a-4bda-9b39-8a501bd22d17)



### Les classes d adresses IPv4


Au début de l'utilisation des adresses IP, seul le premier octet de l’adresse servait à identifier le réseau, créant ainsi 256 réseaux de très grande taille (environ 16 millions d'hôtes chacun). Cependant, cela limitait fortement la flexibilité dans l'attribution des adresses.

La ****RFC 790**** a introduit une division en deux parties : le ****NetID**** (identifiant de réseau) et le ****HostID**** (identifiant de l’hôte). Pour gérer cette division, cinq classes d'adresses (A à E) ont été définies, chaque classe se distinguant par le nombre de bits utilisés pour la partie réseau.

Aujourd'hui, cette classification en classes est obsolète, car les protocoles modernes de routage utilisent ****les masques de sous-réseau**** pour définir de manière explicite la taille du préfixe. Cependant, ces classes sont encore parfois utilisées comme référence historique.

--------------------------------------------------------------------

1) La classe A

****La classe A**** utilise un préfixe de 8 bits pour identifier le réseau. Le premier bit d'une adresse IP de classe A est toujours 0, ce qui fait que la plage du premier octet est comprise entre ****0 et 127****. Cela signifie qu'une adresse IP de classe A commence toujours dans cette plage.

Avec 24 bits restants pour l’adressage des hôtes, une classe A peut théoriquement contenir jusqu'à ****16 777 214 hôtes****. Cependant, la gestion de réseaux aussi vastes est impraticable, et ces adresses sont donc utilisées de manière différente aujourd'hui, notamment en les subdivisant en sous-réseaux plus petits pour une gestion plus efficace.

![image](https://github.com/user-attachments/assets/93bcfef9-886a-4cf7-80b6-5a21c60bb94a)

--------------------------

2) La classe B

La classe B utilise un préfixe de ****16 bits**** pour l'identification du réseau, ce qui laisse également ****16 bits**** pour l'identification des hôtes, permettant ainsi d'adresser jusqu'à ****65 534 hôtes**** par réseau (en tenant compte des adresses réservées).

Les adresses IP de classe B commencent toujours par les deux bits ****10****, ce qui fixe la plage du premier octet entre ****128**** et ****191****. Ainsi, les adresses de classe B vont de ****128.0.0.0**** à ****191.255.255.255****. Cette classe est généralement utilisée pour des réseaux de taille moyenne.

![image](https://github.com/user-attachments/assets/9f4730e0-005d-4f35-987e-e313d3e1d458)

---------------------------

3) La classe C

****La classe C**** est largement utilisée, notamment dans les réseaux domestiques et de petites entreprises. Elle réserve les ****24 premiers bits**** pour le préfixe réseau, laissant ****8 bits**** pour identifier les hôtes, ce qui permet d'avoir jusqu'à ****254 hôtes**** (en excluant les adresses réservées).

Les trois premiers bits des adresses de classe C sont toujours 110, ce qui signifie que le premier octet d'une adresse de classe C est compris entre ****192**** et ****223****. Ainsi, la plage des adresses IP de classe C va de ****192.0.0.**** à ****223.255.255.255****, offrant une taille de réseau bien adaptée aux petites installations.

![image](https://github.com/user-attachments/assets/7040f98f-8f68-4777-bd6d-a30ff0e15411)

-------------------------------

4) La classe D 

****La classe D**** est dédiée au ****multicast****, utilisée pour la diffusion de données à plusieurs récepteurs. Les trois premiers bits d’une adresse de classe D sont toujours 111, et le quatrième est un 0, ce qui donne des adresses comprises entre ****224.0.0.0**** et ****239.255.255.255****.

Contrairement aux classes A, B et C, la classe D n’a pas de distinction entre partie réseau et partie hôte. Les ****4 premiers bits**** sont toujours fixés à ****1110****, tandis que les ****28 bits restants**** désignent un groupe multicast spécifique. Ces adresses ne sont pas attribuées à des hôtes individuels mais à des groupes d’appareils qui se joignent pour recevoir des données envoyées à une adresse multicast.

   Sous-blocs multicast :
   
1) ****224.0.0.0/24**** – appelé ****Local Network Control Block****, réservé par l’IANA pour des protocoles de gestion réseau qui ne traversent pas les routeurs (TTL de 1). Par exemple :

- ****224.0.0.0**** est une adresse réservée.
- ****224.0.0.1**** cible toutes les interfaces sur le réseau local.
- ****224.0.0.2**** cible tous les routeurs sur le réseau local.

2) ****224.0.1.0/24**** – appelé ****Internetwork Control Block****, également réservé pour des protocoles de gestion réseau, mais pouvant franchir les routeurs. Exemple :

- ****224.0.1.1**** est utilisée par ****le protocole NTP**** (Network Time Protocol), pour synchroniser les horloges des appareils sur Internet.

--------------------------

5) La classe E

La classe E est réservée pour des usages futurs ou expérimentaux, sans destination définie à ce jour. Les quatre premiers bits d'une adresse de classe E sont toujours 1111, ce qui place sa plage d'adresses entre ****240.0.0.0**** et ****255.255.255.255****.

Contrairement aux autres classes (A, B, C), la classe E ne précise pas de division entre le préfixe réseau et la partie hôte. Ces adresses ne sont pas assignées pour un usage général sur Internet et sont principalement destinées à des expérimentations ou à des usages spécifiques encore non définis.








### Les types d adresses IPv4




À l'origine, le protocole IP ne distinguait pas les types d'adresses, et toute machine connectée à Internet devait disposer d'une ****adresse IP unique**** et accessible sur l'ensemble du réseau global. Il n'y avait pas de concept d'adresses privées ou réservées pour des usages locaux.

Ce n'est qu'en ****1994****, avec la ****RFC 1597****, que la notion ****d'adresses privées**** a été introduite. Ces adresses permettent à des réseaux internes (comme des réseaux locaux d'entreprises ou domestiques) d'utiliser des plages d'adresses sans avoir à en obtenir d'un registre public.

En ****1996****, la ****RFC 1918**** a formalisé et standardisé l'utilisation de ces adresses privées, les rendant un élément fondamental de l'infrastructure réseau. Cette RFC définit trois plages d'adresses réservées pour les réseaux privés :

- 10.0.0.0 à 10.255.255.255 (classe A)
- 172.16.0.0 à 172.31.255.255 (classe B)
- 192.168.0.0 à 192.168.255.255 (classe C)

Ces adresses privées ne sont pas routées sur Internet et doivent être traduites via un mécanisme comme le ****NAT**** (Network Address Translation) pour accéder à des ressources publiques.


1) Les adresses IP privées


Une ****adresse IP privée**** est attribuée à un hôte au sein d’un réseau interne et n'est pas visible sur Internet. Ce mécanisme a permis de ****ralentir l'épuisement des adresses IPv4**** en autorisant la réutilisation des mêmes plages d’adresses au sein de différents réseaux sans que cela affecte l’unicité des adresses au niveau global.

Les ****adresses privées**** ne sont pas ****routables sur Internet****, ce qui signifie que les fournisseurs d'accès à Internet (FAI) ne transmettent pas ces adresses. Cela oblige les réseaux utilisant des adresses privées à recourir à la ****translation d'adresses**** (NAT, Network Address Translation) pour accéder à Internet. Le NAT permet de ****convertir**** une adresse IP privée en ****adresse IP publique**** lors de l’envoi de paquets sur Internet.

Ainsi, deux réseaux distincts (comme deux entreprises) peuvent utiliser les mêmes plages d’adresses privées sans risque de conflit, car ces adresses ne sont jamais utilisées pour des communications directes entre les deux réseaux.

Les plages privées ont été définies par la ****RFC 1918**** et sont attribuées par classe d’adresses :

- ****10.0.0.0**** à ****10.255.255.255**** (classe A)
- ****172.16.0.0**** à ****172.31.255.255**** (classe B)
- ****192.168.0.0**** à ****192.168.255.255**** (classe C)


Ces plages d'adresses sont réservées pour des réseaux privés et non pour des communications sur Internet.

![image](https://github.com/user-attachments/assets/8f040636-bd91-43d3-8af5-8f89e276140e)


--------------

## 2. Les adresses IP publiques
   
Les ****adresses IP publiques**** sont des adresses qui ne font pas partie des plages privées et sont routables sur Internet. Elles doivent être ****uniques**** pour permettre une communication directe entre différents réseaux sur Internet.

Pour garantir cette unicité, la gestion des adresses IP publiques est régulée par ****l’IANA**** (Internet Assigned Numbers Authority) et les ****RIR**** (Regional Internet Registries). L'IANA détient toutes les plages d'adresses IP publiques et les distribue aux cinq ****RIR**** qui gèrent les différentes régions du monde :

- ****RIPE NCC**** (Europe, Moyen-Orient et certaines parties de l'Asie centrale)
- ****ARIN**** (Amérique du Nord)
- ****APNIC**** (Asie-Pacifique)
- ****LACNIC**** (Amérique latine et Caraïbes)
- ****AFRINIC**** (Afrique)

### Attribution d'adresses publiques

Lorsqu'un ****fournisseur d'accès Internet**** (FAI) a besoin d'une plage d'adresses IP publiques, il doit faire une demande à son RIR régional. Le FAI redistribue ensuite ces adresses à ses clients. Les adresses ainsi attribuées sont appelées ****Provider Dependent**** (PD), car elles dépendent du fournisseur d'accès : si un client change de fournisseur, il perd l'adresse publique qui lui avait été assignée.

Il est également possible d'obtenir des adresses ****Provider Independent**** (PI) directement auprès du RIR, généralement pour des entreprises. Ces adresses permettent de garder la même adresse IP même si l'on change de fournisseur, et de se connecter à plusieurs fournisseurs pour assurer une ****redondance****. Ce type de service est soumis à des conditions strictes et à des frais, mais il offre une plus grande flexibilité et stabilité pour les entreprises qui en ont besoin.

Plages d'adresses IP privées
Les adresses privées sont réservées aux réseaux internes, et voici les plages définies par la ****RFC 1918**** :


![Capture d'écran 2024-10-23 211010](https://github.com/user-attachments/assets/6d1cba36-1e2c-43ca-9d44-b69043d987ca)




Les adresses publiques, quant à elles, sont allouées par les RIR pour permettre la communication sur Internet.







