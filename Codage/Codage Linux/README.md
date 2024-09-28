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


## Le réseau 

### Contient les informations de configuration des interfaces 
`/etc/network/interfaces`

### Affiche le nom de la machine dans le réseau 
`uname -a`

### Teste la connexion réseau avec une machine 
`ping` adresseIP

### Affiche toutes les interfaces réseau disponible 
`ifconfid -a`

### Attribue l'adresse ip à l'interface réseau eth0
`ifconfig` eth adresseIP

### Arrête l'interface réseau eth0
`ifdown` eth0 `ifconfig` eth0 `down`

### Démarre l'interface réseau eth0
`ifup` eth0 `ifconfig` eth0 `up `


### Arrête toutes les connexions Réseau 
`poweroff-i` 

### Définit une passerelle par défaut 
`route add defaut` gw adresseIP 

### Supprime la passerelle par défaut 
`route dek defaut` 

### Configuration de la carte Wifi 
`iwconfig` 


## Bases d'administration 



### Exécute command en mode superutilisateur 
`sudo command ` 

### Idem sudo pour les applications graphique 
`gksudo command` 

### met fin au mode superutilisateur 

`sudo -k`

### Affiche la version du noyau 

`uname -r`

### Redémarrz la machine immédiatement 

`shutdown -h now`

### Affiche les périphérique usb ou pci présents sur la machine 

`isusb`
`ispci`

### Affiche le temps d'exécution de commande 

`time  command`

### Redirige la sortie de commande 1 comme entrée de commande 2 
`commend 1| command 2`

### Efface l'écran du terminal 
`clear`

## Obtenir de l'aide 

### Dossier contenant toutes les documentations 
`/usr/share/doc ` 

### Aide en ligne pour les commandes et de nombreux fichiers de configuration ( q pour quitter) 
`man command `

### Installation des pages d'aide en français 
`apt-get install manpages-fr`

### Récapitulatif de command 
`command -help`


## Se déplacer dans les dossiers 

### Répertoire de travail de utilisateur 
`/home/utilisateur `

### montre le nom du dossier de travail courant 
`pwd `

### se déplacer vers le dossier /home/utilisateur 
`cd`

### Se déplacer vers le dossier /home/utilisateur 
`cd~/Desktop`

### Se déplacer vers le dossier parent 
`cd....`

### Se déplacer vers le dossier/usr/apt 
`cd/usr/apt`  


## Lister les fichiers et répertoires 

### Liste le contenu du répertoire dossier en mode détaillé 
`1s -1 dossier`
`dir -1 dossier `

### Liste tous les fichiers ( y compris les fichiers cachés ) 
1s -a
dir -a

### Lister les répertoires contenu dans le dossier 
1s -d
dir 


