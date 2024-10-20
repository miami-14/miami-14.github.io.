# L'adressage Rthernet  

## L’adresse IPv4 et le masque de sous­réseau

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

le résultat est différent et il indique qu’une machine avec une adresse IPv4 192.168.128.10 et un masque de 255.255.248.0 fait partie du réseau 192.168.128.0.

Par conséquence, la machine 192.168.128.10 ne fait pas partie du même réseau que la machine 192.168.1.1 lorsque le masque 255.255.248.0 est utilisé


les exemples précédents, le masque a été représenté de manière binaire et de manière numérique.

existe une troisième manière, parfois plus pratique, de représenter le masque aux côtés de l’adresse réseau, cette notation est appelée CIDR

on note par exemple 192.168.128.0/21 pour signifier que le masque contient 21 bits et
que l’adresse réseau est 192.168.128.x. On parle alors aussi de préfixe réseau ou de taille de préfixe.


## La longueur de préfixe et la taille de réseau


La longueur de préfixe fait référence au nombre de bits utilisés pour identifier le réseau dans une adresse IP. Elle est souvent représentée sous forme de notation CIDR (Classless Inter-Domain Routing), par exemple, /24, ce qui signifie que les 24 premiers bits représentent la partie réseau.

La taille de réseau correspond au nombre d'adresses disponibles dans un réseau. Elle dépend de la longueur du préfixe : plus le préfixe est court (par exemple /16), plus le réseau est grand, car il y a plus d'adresses IP disponibles pour les hôtes.


Il y a valeurs deux sont réservées

- L’adresse dont tous les bits hôtes valent 0, cette adresse est utilisée pour représenter le réseau.

- L’adresse dont tous les bits hôtes valent 1, cette adresse est utilisée pour représenter le Broadcast.

![image](https://github.com/user-attachments/assets/b7097ee5-9724-4cf4-a466-1ebf9b1553f3)

![image](https://github.com/user-attachments/assets/0897bde2-779a-44c4-bfb3-376444a5f4b2)


L’adresse réseau est utilisée pour représenter... un réseau, cette adresse est composée uniquement de 0 sur sa partie hôte et elle ne peut pas être attribuée à une interface. En reprenant le diagramme du chapitre La couche Réseau ­ Les fonctions de la couche Réseau, il est possible d’y ajouter les réseaux afin d’avoir une carte de la topologie au niveau IP.

![image](https://github.com/user-attachments/assets/a60215db-5d5a-4bda-9b39-8a501bd22d17)
