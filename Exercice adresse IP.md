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

Exercice 3: 

Les masques de sous-réseaux par défaut dépendent de la classe de l'adresse IP. Voici les classes d'adresses IP et leurs masques de sous-réseaux par défaut :

- Classe A : 1.0.0.0 à 126.0.0.0, masque par défaut 255.0.0.0 (ou /8).

- Classe B : 128.0.0.0 à 191.255.0.0, masque par défaut 255.255.0.0 (ou /16).

- Classe C : 192.0.0.0 à 223.255.255.0, masque par défaut 255.255.255.0 (ou /24).

- Classe D (multidiffusion) : 224.0.0.0 à 239.255.255.255.

- Classe E (réservée pour la recherche) : 240.0.0.0 à 255.255.255.255.


      Voici les masques de sous-réseaux par défaut pour les adresses données :

- 124.95.45.1 (Classe A) : 255.0.0.0

- 100.0.145.1 (Classe A) : 255.0.0.0

- 182.0.179.254 (Classe B) : 255.255.0.0

- 128.190.223.154 (Classe B) : 255.255.0.0

- 191.18.200.149 (Classe B) : 255.255.0.0

- 192.205.110.99 (Classe C) : 255.255.255.0

--------------------------------------------

    Exercice n°5 : Pour déterminer la partie réseau et la partie hôte des adresses IP données, nous devons utiliser les masques de sous-réseaux par défaut associés à chaque classe d'adresse IP. Voici les classes d'adresses IP et leurs masques :


- Classe A : Masque 255.0.0.0 (ou /8) : 1er octet pour le réseau, 3 octets pour l'hôte.
- Classe B : Masque 255.255.0.0 (ou /16) : 2 premiers octets pour le réseau, 2 octets pour l'hôte.
- Classe C : Masque 255.255.255.0 (ou /24) : 3 premiers octets pour le réseau, 1 octet pour l'hôte.

      En se basant sur les masques de sous-réseaux par défaut, donnez la partie réseau et la partie
      hôte des adresses IP suivantes :

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


            Pour déterminer si une adresse IP est valide pour un hôte TCP/IP, il est nécessaire de vérifier si l'adresse respecte les règles suivantes :

- L'adresse IP ne doit pas être une adresse de réseau (le dernier octet est 0) ou une adresse de diffusion (le dernier octet est 255).

- L'adresse IP doit respecter les limites des classes d'adresses.

- Chaque octet doit être compris entre 0 et 255.

          Exercice n°6 : Indiquez si les adresses suivantes sont valides ou pas pour un hôte TCP/IP. Le masque est
          celui associé par défaut à la classe d'adresse.

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

    Exercice 7 : Passez les adresses IP suivantes de la notation CIDR à la notation décimale pointée :

