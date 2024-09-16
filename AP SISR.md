# AP SISR 

 putty =>  mia -> mia /
           root-> root

![Capture_d’écran_2024-09-16_103838_AP1](https://github.com/user-attachments/assets/d2cad5e1-5d76-4d8c-b932-23498ee6c03c)

# AP 1
## Exercice 1 

1 ) Sous un format condensé. 

- `ls` ( le nom des ressources ) 


![Capture_d’écran_2024-09-16_110932_AP_2](https://github.com/user-attachments/assets/262fad35-0347-4c11-8767-789fc086b35b)



2 ) Sous un format long ( donnant le propriétaire, les permissions, la taille, ...). 

- `ls -l` ( Affiche les fichiers sous forme de liste longue. )





3 ) En affichant les fichiers Cacher  ( dont commence par un point).

- `ls -a` 

4 ) En colorant le type des fichiers et en ordre inverse.

- `ls -l --color`

  
![Capture_d’écran_2024-09-16_110932_AP_2](https://github.com/user-attachments/assets/1c1ffaac-176e-44c7-8457-cf685ae8d58e)


- `ls -l --color /etc`

![Capture_d’écran_2024-09-16_111007_AP_3_](https://github.com/user-attachments/assets/0c007fe6-6e58-47f7-a76e-b3cbab2b0f3d)
  
5 ) Avec un format long et en affichant les fichiers cachés, mais du plus récent au plus ancien. 

- `ls -l -t`

![Capture_d’écran_2024-09-16_111535_AP_4](https://github.com/user-attachments/assets/4df52d2d-c5b4-4257-9f22-fa31ff8ca201)


  
- `ls -l -t /etc`

![Capture_d’écran_2024-09-16_111449_AP_5](https://github.com/user-attachments/assets/3993d0f6-724d-4921-835c-13e723d44f17)


  

6 ) Avec un format long et en affichant les fichiers cachés, mais du plus ancien au plus récent.

- `ls -l -a -t`

  ![Capture_d’écran_2024-09-16_112322_AP_6](https://github.com/user-attachments/assets/322a1746-5689-4104-af8f-5e755e70e806)




## Exercice 2 : Où que vous soyez, quel est l'effet de la commande cd sans paramètre ? 

![Capture_d’écran_2024-09-16_113019_AP_EX_2_1](https://github.com/user-attachments/assets/83cb9255-18ef-4db8-90f3-9c9dae7a90b5)


![Capture_d’écran_2024-09-16_113202_AP_EX2_2](https://github.com/user-attachments/assets/1599ecd0-7f9c-4484-8889-c631319da200)



## Exercice 3 : Dans votre répertoire courant, créez en une commande les fichiers suivants : 

annee1   annee2    annee4   annee45  annee41   annee510 

-  `touch annee1`
-  `touch annee2`
-  `touch annee4`
-  `touch annee45`
-  `touch annee41`
-  `touch annee510` 

![Capture_d’écran_2024-09-16_131126_EX_3_1](https://github.com/user-attachments/assets/fd33b41a-3afc-459e-b714-80fce5f25e93)



Si je veux supprimer `rm`


## Exercie 4 : Créez le répertoire Year dans votre répertoire courant, puis en une seule 

Commende d"placez les fichiers précédement créés dans le répertoire Year.

-  `mv [aA]* /home/mia`


![Capture_d’écran_2024-09-16_131622_EX_4_](https://github.com/user-attachments/assets/29238ce2-bc37-4517-95c6-a5d47c7276eb)

## Exercice 5 : 

1 ) Créez un répertoire systeme sous votre dossier personnel (homedir), puis un répertoire TP1 dans systeme. 

  - `mkdir systeme`
![Capture_d’écran_2024-09-16_132628_EX_5_1](https://github.com/user-attachments/assets/9f0638a8-9149-41ff-a80b-0093f50f4173)


![Capture_d’écran_2024-09-16_134409_EX5_2](https://github.com/user-attachments/assets/694ae635-0101-46aa-8e99-9140d0fe02c0)

 
  
  - `mdkri systeme /TP1`

![Capture_d’écran_2024-09-16_134448_EX_5_3](https://github.com/user-attachments/assets/2334c558-3663-4f50-bc16-5aede90d76e6)



    


2 ) Effecez  le répertoire systeme avec la commande rmdir. Que constatez-vous ? 

 - `rmdir systeme`

![Capture_d’écran_2024-09-16_134558_EX_5_4](https://github.com/user-attachments/assets/c10e31d1-6d0b-4342-8404-80517ba6a77c)



   Je ne peux pas supprimer le système car il surpprimer que des dossiers cide

   `rmdir` : supprimer un repertoire vide
   
![Capture_d’écran_2024-09-16_134633_EX_5_5_](https://github.com/user-attachments/assets/8b579e84-d18f-41b0-a204-94dc17da2415)



3 ) Après avoir effacé les répertoires tp1 et system, créez à l'aide d'une seule commande les répertoires system, system/tp1, system/tp2 

 -  `mkdir -p system/TP1 systeme/TP2`

![Capture_d’écran_2024-09-16_134713_EX_5_6_](https://github.com/user-attachments/assets/1b69ee1d-397f-412a-94af-63456ea1d995)



4 ) Renommez le répertoire systeme en test.

- `mv systeme test`


  ![Capture_d’écran_2024-09-16_135242_EX_8](https://github.com/user-attachments/assets/3beebf8a-caf3-4706-8a46-d8fc77264aea)

![Capture_d’écran_2024-09-16_134741_EX_5_7](https://github.com/user-attachments/assets/fc113d79-0c37-4579-9ad4-77444d2d294b)



1 ) En faisant la copuie depuis le répertoire /bin 

- `cd /bin `


![Capture_d’écran_2024-09-16_142858_EX_5_9](https://github.com/user-attachments/assets/a587dfc6-06f9-4a39-9f59-ce12ebf923c9)



  

- `cp host /home/mia/testTP1`

![Capture_d’écran_2024-09-16_142944_EX_5_10](https://github.com/user-attachments/assets/dd1f2e38-bd63-4833-8710-7c45fb17747a)


2) En faisant la copie depuis le répertoire test /TP1

  - `cd /home/mia/test/TP1`
    
![Capture_d’écran_2024-09-16_143029_EX_5_11](https://github.com/user-attachments/assets/f81b7511-b619-4e8e-80f3-4e02e2a2d418)

  
  - `cp /bin/host host`

![Capture_d’écran_2024-09-16_143059_EX_5_12](https://github.com/user-attachments/assets/7b9b825a-f704-4a5e-ba4f-ad6495a94521)


![Capture_d’écran_2024-09-16_143146_EX_5_13](https://github.com/user-attachments/assets/9140d085-eb1c-487c-841b-70c6d501cd9f)


3) Effacez à l'aide d'une seule commandeles répertoires test/TP1 et test/TP2

   - `rm -R /home/mia/test/TP*`

![Capture_d’écran_2024-09-16_143732_EX_5_14(1) (1)](https://github.com/user-attachments/assets/eb51a9f8-232a-452d-ab03-9c58b4d185be)




# AP 2 


## Exercice 1 : Déterminé les commandes permettant de réaliser lee actions suivantes : 

1 ) Déterminer le répertoire par défaut dans la hiérarchie des répertoires ? 
![Capture_d’écran_2024-09-16_161936_AP_2_EX_1_](https://github.com/user-attachments/assets/2e16d80d-c618-4bc9-a1f0-70d014618663)



2 ) Y a t-il des fichiers, des répertoires dans ce répertoire ?

![Capture_d’écran_2024-09-16_162326_AP_2_EX2](https://github.com/user-attachments/assets/93f81586-8907-4381-9a6f-692c6f8dbf12)



3 ) Entrer du texte dans un fichier nommé « Mon_fichier » que vous avez créé au 
préalable.

![Capture_d’écran_2024-09-16_162405_AP_2_EX3](https://github.com/user-attachments/assets/c90d4e95-3be5-4af0-9fa4-2f8eda8cfad9)



4 ) Lister le contenu de `"Mon_fichier"`
![Capture_d’écran_2024-09-16_162440_AP_2_EX_4 (1)](https://github.com/user-attachments/assets/1f44c6a0-ff6a-4262-8c29-fb461fa8cf16)


5 ) Lister le répertoire courant.



6 ) Lister les répertoires /bin et /dev

`/bin `
![Capture_d’écran_2024-09-16_162534_AP_2_EX5](https://github.com/user-attachments/assets/c978dd5e-cd20-4329-ae7d-a0e0e11ff36a)


`/dev`
![Capture_d’écran_2024-09-16_162627_AP_2_EX5](https://github.com/user-attachments/assets/6fe5b79c-b5bc-46bd-bb14-20b16766d68b)



7 ) Créer sous votre répoitre deux sous-répertoires : " Source " et "Data" 

![Capture_d’écran_2024-09-16_162727_AP_2_EX6](https://github.com/user-attachments/assets/977359ad-de76-4ff0-bb7d-082b2f33efe9)



8 ) Se positionner sous " Source"


![Capture_d’écran_2024-09-16_162831_AP_2_EX_7](https://github.com/user-attachments/assets/bca5f254-84ae-4261-9088-6c5291fb25b1)


9 ) Listez le répertoire courant 

![Capture_d’écran_2024-09-16_162910_AP_2_EX_8](https://github.com/user-attachments/assets/76723b8b-9a8c-4723-b00c-472c5dcdbdd6)



10 ) Revenir sous me répertoire de départ et détruire " Source "

![Capture_d’écran_2024-09-16_163009_AP_2_EX_9](https://github.com/user-attachments/assets/5bc27ab8-700a-47e9-af85-69893efecbcb)


11 )  Créer un deuxième fichier nommé « Mon_fichier_2 ».

![Capture_d’écran_2024-09-16_163009_AP_2_EX_9](https://github.com/user-attachments/assets/72dcfe65-fe2c-4471-b57f-affc060bd891)


12 ) Copier chaque fichier en nom_de_fichier.old.


![Capture_d’écran_2024-09-16_164529](https://github.com/user-attachments/assets/d7adde03-1853-433b-b1b9-bd80c6f9ea9c)


13 ) Créer un répertoire « Old »


14 ) Déplacer les fichiers avec l'extension .old vers le répertoire « Old ».



15 ) Effacer tous les fichiers crées dans Old sans effacer le répertoire Old. 

 









  

