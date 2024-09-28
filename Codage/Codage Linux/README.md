# Codage Linux 

## Les paquets

### Fichier contenant la liste des dépôts 

`/etc/apt/sources.list`

### Met à jour la liste des paquets disponibles à partir de sources.list 

`apt-get-update`

### Met à jour les paquets déjà installés 

`apt-get upgrade`

### Met à jour votre distribution Ubuntu vers la vers la version supérieure 

`apt-get dist-upgrade`

### Installe le logiciel soft en gérant les dépendances 
`apt-get install` soft


### Désinstallé le paquet soft et toutes ses dépendances

`apt-get remove` soft

### Supprime le paquet soft et ses fichiers de configuration 

`apt-get remove -purge `soft


### Supprime les copies des paquets désinstallés 

`apt-get autoclean`


### Affiche une liste des paquets disponible 

`apt-cache dumpavail`

### Donne la liste des paquets dont le nom ou la description contient soft

`apt-cache search `soft

### Affiche la description du paquet soft 

`apt-cache show `soft 

### Affiche des informations sur le paquet soft   

`apt-cache showpkg `soft 

### Liste les paquets requise par soft

`apt-cache depend` soft 


### Liste les paquets qui requièrent le paquet soft 

`apt-cache rdepends` soft


### Met à jour les informations à partir de fichiers sources liste 

`apt-file update` 

### Recherche à quel paquet fichier appartient 

`apt-file search` fichier

### Liste les fichiers contenus dans le paquet soft 

`apt-file list` soft

### Liste les paquets orphelins

`deborplan`

### Convertir paquet est en paquet deb (-d) et installe le paquet (-1)

`alien-di paquet ext`

### Installe le paquet ( ne gère pas les dépendances ) 

`dpkg -i paquet deb`

### Liste le contenu du paquet 

`dpkg -c pauet.deb`

### Affiche les informations du paquet 
`dpkg -I paquet.deb` 
