# Exercice adresse IP



    Exercice 1: Convertissez en binaire les adresses IP suivantes :

1) 82.166.19.3 :
- 82 = 01010010
- 166 = 10100110
- 19 = 00010011
- 3 = 00000011
- Binaire : ****01010010.10100110.00010011.00000011****


3) 127.0.0.1 :
- 127 = 01111111
- 0 = 00000000
- 0 = 00000000
- 1 = 00000001
- Binaire : ****01111111.00000000.00000000.00000001****

4) 135.224.27.95 :
- 135 = 10000111
- 224 = 11100000
- 27 = 00011011
- 95 = 01011111
- Binaire : ****10000111.11100000.00011011.01011111****

5) 172.31.46.56 :
- 172 = 10101100
- 31 = 00011111
- 46 = 00101110
- 56 = 00111000
- Binaire : ****10101100.00011111.00101110.00111000****

6) 195.200.60.48 :
- 195 = 11000011
- 200 = 11001000
- 60 = 00111100
- 48 = 00110000
- Binaire : ****11000011.11001000.00111100.00110000****

7) 218.75.36.5 :
- 218 = 11011010
- 75 = 01001011
- 36 = 00100100
- 5 = 00000101
- Binaire : ****11011010.01001011.00100100.00000101****

----------------------

    Exercice 2 : Convertissez en décimal pointé les adresses IP suivantes

1) 11100101.10100110.01000101.00100101 :
- 11100101² = 229
- 10100110² = 166
- 01000101² = 69
- 00100101² = 37
Décimal pointé : ****229.166.69.37****


2) 11010100.10101000.10100101.00101001 :
- 11010100² = 212
- 10101000² = 168
- 10100101² = 165
- 00101001² = 41 
Décimal pointé : ****212.168.165.41****


3) 10100101.10100010.10100010.00100010 :
- 10100101² = 165
- 10100010² = 162
- 10100010² = 162
- 00100010² = 34
Décimal pointé : ****165.162.162.34****


4) 10100101.11000000.11100001.00111111 :
- 10100101² = 165 
- 11000000² = 192
- 11100001² = 225
- 00111111² = 63 
Décimal pointé : ****165.192.225.63****


5) 10010011.11101101.11010110.00101001 :
- 10010011² = 147
- 11101101² = 237
- 11010110² =214
- 00101001² = 41
Décimal pointé : ****147.237.214.41****


6) 11110101.11010010.11011101.00110100 :
- 11110101² = 245 
- 11010010² = 210
- 11011101² = 221
- 00110100² = 52 
Décimal pointé: ****245.210.221.52****

---------------------------------

    Exercice 3: Donnez les classes d'adresses pour les adresses suivantes :

Les masques de sous-réseaux par défaut dépendent de la classe de l'adresse IP. Voici les classes d'adresses IP et leurs masques de sous-réseaux par défaut :

- Classe A : 1.0.0.0 à 126.0.0.0, masque par défaut 255.0.0.0 (ou /8).

- Classe B : 128.0.0.0 à 191.255.0.0, masque par défaut 255.255.0.0 (ou /16).

- Classe C : 192.0.0.0 à 223.255.255.0, masque par défaut 255.255.255.0 (ou /24).

- Classe D (multidiffusion) : 224.0.0.0 à 239.255.255.255.

- Classe E (réservée pour la recherche) : 240.0.0.0 à 255.255.255.255.


      Voici les masques de sous-réseaux par défaut
      pour les adresses données :

- 124.95.45.1 (Classe A) : 255.0.0.0

- 100.0.145.1 (Classe A) : 255.0.0.0

- 182.0.179.254 (Classe B) : 255.255.0.0

- 128.190.223.154 (Classe B) : 255.255.0.0

- 191.18.200.149 (Classe B) : 255.255.0.0

- 192.205.110.99 (Classe C) : 255.255.255.0

--------------------------------------------

    Exercice n°5 : Donnez les masques de sous-réseaux par défaut des adresses
    suivantes :

    Pour déterminer la partie réseau et la partie hôte des adresses IP 
    données, nous devons utiliser les masques de sous-réseaux par défaut 
    associés à chaque classe d'adresse IP. Voici les classes d'adresses IP
    et leurs masques :


- Classe A : Masque 255.0.0.0 (ou /8) : 1er octet pour le réseau, 3 octets pour l'hôte.
- Classe B : Masque 255.255.0.0 (ou /16) : 2 premiers octets pour le réseau, 2 octets pour l'hôte.
- Classe C : Masque 255.255.255.0 (ou /24) : 3 premiers octets pour le réseau, 1 octet pour l'hôte.

      En se basant sur les masques de sous-réseaux par défaut,
      donnez la partie réseau et la partie hôte des adresses IP
      suivantes :

- 168.234.150.19 (Classe B):
Partie réseau : 168.234
Partie hôte : 150.19

- 65.200.45.99 (Classe A) :
Partie réseau : 65
Partie hôte : 200.45.99

- 202.130.199.1 (Classe C):
Partie réseau : 202.130.199
Partie hôte : 1

- 193.130.224.254 (Classe C):
Partie réseau : 193.130.224
Partie hôte : 254

- 191.218.20.4 (Classe B):
Partie réseau : 191.218
Partie hôte : 20.4

- 195.209.140.69 (Classe C):
Partie réseau : 195.209.140
Partie hôte : 69

-----------------------------------

        Exercice n°6 : Indiquez si les adresses suivantes sont valides ou 
        pas pour un hôte TCP/IP. Le masque est celui associé par défaut à 
        la classe d'adresse.

        Pour déterminer si une adresse IP est valide pour un hôte TCP/IP,
        il est nécessaire de vérifier si l'adresse respecte les règles suivantes :

- L'adresse IP ne doit pas être une adresse de réseau (le dernier octet est 0) ou une adresse de diffusion (le dernier octet est 255).

- L'adresse IP doit respecter les limites des classes d'adresses.

- Chaque octet doit être compris entre 0 et 255.

 
         Voici l'analyse des adresses données :         

- 1)245.123.133.102 (Classe E):
Validité : Non valide (Classe E est réservée pour des usages futurs)

- 2) 123.123.123.123 (Classe A):
Validité : Valide (Pas d'adresse de réseau ni de diffusion)

- 3) 198.234.17.255 (Classe C):
Validité : Non valide (C'est une adresse de diffusion pour le réseau 198.234.17.0)

- 4) 198.23.254.0 (Classe C):
Validité : Non valide (C'est une adresse de réseau pour le réseau 198.23.254.0)

- 5) 156.26.12.103 (Classe B):
Validité : Valide (Pas d'adresse de réseau ni de diffusion)

- 6) 90.0.0.12 (Classe A):
Validité : Valide (Pas d'adresse de réseau ni de diffusion)

--------------------------------------

    Exercice 7 : Passez les adresses IP suivantes de la notation CIDR à la notation décimale         pointée :

Pour convertir les adresses IP de la notation CIDR à la notation décimale pointée, nous devons déterminer le masque de sous-réseau correspondant au nombre de bits réseau donné après le /. Ensuite, nous convertissons ce masque en notation décimale pointée.

    Voici le processus de conversion :

/12 signifie que les 12 premiers bits sont pour le réseau.
/30 signifie que les 30 premiers bits sont pour le réseau, et ainsi de suite.


    Conversion des adresses CIDR en notation décimale pointée :

25.45.12.200/12 :
- Masque CIDR : /12 correspond à 255.240.0.0 (12 bits de 1)
- Adresse IP avec masque : 25.45.12.200/255.240.0.0

75.230.130.24/30 :
- Masque CIDR : /30 correspond à 255.255.255.252 (30 bits de 1)
- Adresse IP avec masque : 75.230.130.24/255.255.255.252

120.250.65.99/14 :
- Masque CIDR : /14 correspond à 255.252.0.0 (14 bits de 1)
- Adresse IP avec masque : 120.250.65.99/255.252.0.0

136.45.78.199/13 :
- Masque CIDR : /13 correspond à 255.248.0.0 (13 bits de 1)
- Adresse IP avec masque : 136.45.78.199/255.248.0.0

180.64.15.220/20 :
- Masque CIDR : /20 correspond à 255.255.240.0 (20 bits de 1)
- Adresse IP avec masque : 180.64.15.220/255.255.240.0

191.198.24.1/22 :
- Masque CIDR : /22 correspond à 255.255.252.0 (22 bits de 1)
- Adresse IP avec masque : 191.198.24.1/255.255.252.0


--------------------------------------------------


    Exercice 1 :

Une station a pour adresse IP = 192.168.100.32
Son masque de sous-réseau est 255.255.255.0

            - 1) A quelle classe appartient cette adresse ?
L'adresse 192.168.100.32 commence par 192, ce qui la place dans la classe C (classe C : 192.0.0.0 à 223.255.255.255). Classe : C


            - 2) Quel est le numéro de réseau (NetId) ?
Le NetId correspond à la partie réseau de l'adresse, déterminée par le masque de sous-réseau. Dans ce cas, le masque de sous-réseau est 255.255.255.0, ce qui signifie que les 3 premiers octets (24 bits) représentent la partie réseau.
NetId : 192.168.100


            - 3) Quelle est l’adresse de réseau ?
L'adresse de réseau est obtenue en appliquant un ET logique entre l'adresse IP et le masque de sous-réseau. Pour ce cas, cela revient à conserver les trois premiers octets, et à mettre à 0 le dernier octet de l'adresse IP (car le masque pour le dernier octet est 0).
Adresse de réseau : 192.168.100.0


            - 4) Quel est le numéro de machine dans ce réseau (HostId) ?
Le HostId représente la partie hôte de l'adresse IP. Avec un masque de sous-réseau de 255.255.255.0, le dernier octet (8 bits) est la partie dédiée aux hôtes. Dans ce cas, le dernier octet de l'adresse IP est 32.
HostId : 32


            - 5) Combien d’adresses IP sont utilisables dans ce cas pour un Hôte TCP/IP ?
Le masque de sous-réseau est 255.255.255.0, ce qui laisse 8 bits pour la partie hôte. Le nombre total d'adresses possibles pour les hôtes est donné par 2 Puissance 8 =256 Cependant, deux adresses sont réservées :

- L'adresse de réseau (dans ce cas, 192.168.100.0).

- L'adresse de diffusion (dans ce cas, 192.168.100.255).

Donc, le nombre d'adresses utilisables pour les hôtes est 256 - 2= 254 

Nombre d'adresses IP utilisables : 254


        - 6) Quelle est l’adresse de diffusion dans ce réseau ?
L'adresse de diffusion est l'adresse qui correspond à tous les bits de la partie hôte mis à 1. Avec un masque de 255.255.255.0, la partie hôte est représentée par le dernier octet, et si tous les bits sont à 1, cela donne 255.

- Adresse de diffusion : 192.168.100.255

        Résumé des réponses :
- Classe : C
- NetId : 192.168.100
- Adresse de réseau : 192.168.100.0
- HostId : 32
- Adresses IP utilisables : 254
- Adresse de diffusion : 192.168.100.255


----------------------------------------------

    Exercice 2 :

Une station a pour adresse IP = 152.120.35.30
Son masque de sous-réseau est 255.255.240.0

        - 1) A quelle classe appartient cette adresse ?
L'adresse 152.120.35.30 commence par 152, ce qui la place dans la classe B (classe B : 128.0.0.0 à 191.255.255.255). Classe : B

            - 2) Quel est le numéro de sous-réseau (NetId) ?
Le NetId est obtenu en appliquant le masque de sous-réseau à l'adresse IP. Le masque 255.255.240.0 signifie que les 20 premiers bits sont pour la partie réseau. Le masque sépare les bits de la manière suivante :

- Les deux premiers octets (152.120) sont pour la partie réseau (fixe pour la classe B).
- Le masque utilise les 4 premiers bits du troisième octet pour le sous-réseau. Les 4 derniers bits du troisième octet, ainsi que le dernier octet, sont pour la partie hôte.

        Pour trouver le NetId, on effectue un ET logique entre l'adresse IP et le masque :

- Adresse IP : 152.120.35.30 (en binaire : 10011000.01111000.00100011.00011110)
- Masque : 255.255.240.0 (en binaire : 11111111.11111111.11110000.00000000)

        Effectuons l'ET logique entre l'adresse et le masque :

- Résultat en binaire : 10011000.01111000.00100000.00000000

        Ce qui correspond à 152.120.32.0 en décimal.

- Numéro de sous-réseau (NetId) : 152.120.32


        - 3) Quelle est l’adresse de sous-réseau ?
L'adresse de sous-réseau correspond au résultat de l'ET logique entre l'adresse IP et le masque de sous-réseau. C'est le même résultat que le NetId.

-Adresse de sous-réseau : 152.120.32.0

        - 4) Quel est le numéro de machine dans ce sous-réseau (HostId) ?
Le HostId représente la partie hôte de l'adresse IP. Avec le masque ****255.255.240.0****, les 12 derniers bits sont réservés pour les hôtes. Il faut donc extraire ces bits de l'adresse IP pour obtenir le numéro de la machine.

- Adresse IP en binaire : 10011000.01111000.00100011.00011110

- Les 12 derniers bits (000111.00011110) correspondent au HostId, qui donne 3.30 en décimal.

- HostId : 3.30

  
        - 5) Combien peut-il y avoir de sous-réseaux ?
  Dans une adresse de classe B, le masque par défaut est 255.255.0.0 (ou /16). Ici, le masque utilisé est 255.255.240.0 (ou /20). La différence entre /16 et /20 est de 4 bits supplémentaires utilisés pour les sous-réseaux.

Le nombre de sous-réseaux possibles est donné par 2puissance 4 = 16

- Nombre de sous-réseau possible : 16

  
        6) Quelle est l’adresse de diffusion dans ce sous-réseau ?
L'adresse de diffusion est obtenue en mettant tous les bits de la partie hôte à 1. Dans ce cas, avec un masque 255.255.240.0, les 12 derniers bits sont réservés pour la partie hôte.

    Si on met tous ces bits à 1, l'adresse de diffusion devient :

- Adresse réseau : 152.120.32.0
- Partie hôte maximale : 0.15.255 (car les 12 bits de la partie hôte sont tous à 1)

        Donc, l'adresse de diffusion est 152.120.47.255.

- Adresse de diffusion : 152.120.47.255

        Résumé des réponses :
- Classe : B
- NetId : 152.120.32
- Adresse de sous-réseau : 152.120.32.0
- HostId : 3.30
- Nombre de sous-réseaux possibles : 16
- Adresse de diffusion : 152.120.47.255

-----------------------------------------------------

    1) Soit l'adresse 192.16.5.133/29.
    
Combien de bits sont utilisés pour identifier la partie réseau ?

Combien de bits sont utilisés pour identifier la partie hôte ?

    2) Soit l'adresse 172.16.5.10/28.
    
Quel est le masque réseau correspondant ?


    3) On attribue le réseau 132.45.0.0/16. Il faut redécouper ce réseau en 8
    sous-réseaux.

a. Combien de bits supplémentaires sont nécessaires pour définir huit sous-
réseaux ?

b. Quel est le masque réseau qui permet la création de huit sous-réseaux ?

c. Quelle est l'adresse réseau de chacun des huit sous-réseaux ainsi définis ?

d. Quelle est la plage des adresses utilisables du sous-réseau numéro 3 ?

e. Quelle est l'adresse de diffusion du sous-réseau numéro 4 ?

---------------------------------------------------------

    Exercice 1 : A quelle classe appartient l'adresse 180.30.17.20 ? Justifiez.

L'adresse 180.30.17.20 appartient à la classe B.
Car Les adresses IP sont divisées en plusieurs classes, basées sur la plage des valeurs du premier octet (le premier nombre de l'adresse).

    Classes d'adresses IP :

Classe A : 1.0.0.0 à 126.255.255.255 (premier octet entre 1 et 126).
Classe B : 128.0.0.0 à 191.255.255.255 (premier octet entre 128 et 191).
Classe C : 192.0.0.0 à 223.255.255.255 (premier octet entre 192 et 223).

    Analyse de l'adresse 180.30.17.20 :

Le premier octet de l'adresse est 180.
Le nombre 180 se situe dans la plage de 128 à 191, ce qui correspond à la classe B.
Donc, 180.30.17.20 est une adresse de classe B.

Les adresses de classe B ont un masque par défaut de 255.255.0.0, où les deux premiers octets représentent la partie réseau, et les deux derniers octets sont réservés pour la partie hôte.


    Exercice 2 :Pour chaque adresse, entourez la partie demandée :

1• PARTIE RESEAU : 1.102.45.177 
-Classe A car le premier octet est 1 
-La partie réseau est le premier octet : 1.
-Partie réseau : 1

2• PARTIE HOTE : 196.22.177.13 
-Le premier octet est 196, donc c'est une classe C.
-La partie hôte est le dernier octet : 13.
-Partie hôte : 13


3• PARTIE RESEAU : 133.156.55.102
-Le premier octet est 196, donc c'est une classe B.
-La partie réseau est les deux premiers octets : 133.156..
-Partie réseau : 133.156


4• PARTIE HOTE : 221.252.77.10
-Le premier octet est 221, donc c'est une classe C.
-La partie hôte est le dernier octet : 10.
-Partie hôte : 10


5• PARTIE RESEAU : 123.12.45.77
-Le premier octet est 123, donc c'est une classe A..
-LLa partie réseau est le premier octet : 123.
-Partie réseau : 123


6• PARTIE HOTE : 126.252.77.103
-Le premier octet est 126, donc c'est une classe A.
-La partie hôte est les trois derniers octets : 252.77.103.
-Partie hôte : 252.77.103


7• PARTIE RESEAU : 13.1.255.102
-Le premier octet est 13, donc c'est une classe A.
-La partie réseau est le premier octet : 13.
-Partie réseau : 13

8• PARTIE HOTE : 171.242.177.109
-Le premier octet est 171, donc c'est une classe B.
-La partie hôte est les deux derniers octets : 177.109.
-Partie hôte : 177.109

## Résumé :
- Partie réseau : 1
- Partie hôte : 13
- Partie réseau : 133.156
- Partie hôte : 10
- Partie réseau : 123
- Partie hôte : 252.77.103
- Partie réseau : 13
- Partie hôte : 177.109




        Exercice 3 :Un réseau de classe B est découpé en plusieurs sous-réseaux et on obtient             un masque final valant 255.255.252.0. En combien de sous-réseaux le réseau de départ             a-t-il été découpé ?

- []a) 32
- [x]b) 64
- []c) 128
- []d) 256

![image](https://github.com/user-attachments/assets/8c576786-f62c-43f0-bf08-317444a59d91)

![Capture d'écran 2024-10-23 231039](https://github.com/user-attachments/assets/e39aeb36-5dc2-47ad-a631-bb5b2f3d25d7)


    Exercice 4 :Un réseau a comme masque 255.255.255.224. Combien de machines peut-il y avoir         sur un tel réseau ? Justifiez.

![image](https://github.com/user-attachments/assets/63ff0e21-4431-4afe-98cf-a0d8ba068c24)

![image](https://github.com/user-attachments/assets/21d4c591-ed3f-4630-ab88-167616804dee)

    Exercice 5 :Une machine a comme adresse IP 150.56.188.80 et se trouve dans un réseau dont         le masque est 255.255.240.0. Quelle est l'adresse du réseau ? Justifiez.

![image](https://github.com/user-attachments/assets/21f23351-654c-4433-9518-055d8aba140e)

![image](https://github.com/user-attachments/assets/2c94f79e-4aa8-4aa0-8e47-a7676b4dc04e)

![image](https://github.com/user-attachments/assets/609e9605-4814-4173-8d18-b757c8321fa9)

![image](https://github.com/user-attachments/assets/fb9a9a78-c21e-441f-bc33-cbdcee7f746b)

  
    
    Exercice 6 :Découpez en 14 sous-réseaux le réseau 150.27.0.0 de
    masque 255.255.0.0 Indiquez pour chaque sous-réseau la plage
    des adresses attribuables à une machine ainsi que l’adresse de diffusion.  
    Justifiez votre réponse.

![image](https://github.com/user-attachments/assets/6afa978f-70a9-4ee2-9893-12b05f9b4adc)

![image](https://github.com/user-attachments/assets/dc01220e-d89a-4eb8-b3e1-7fa923191049)

![image](https://github.com/user-attachments/assets/635b4584-5479-4a42-bd79-22c57d9cc027)

![image](https://github.com/user-attachments/assets/2ff38ee9-5cbf-4f32-b5d8-a7c1dc3eb897)

![image](https://github.com/user-attachments/assets/7f6f4fdc-6ea5-41d8-9106-c4d4fd2ec15c)
