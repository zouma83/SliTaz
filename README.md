# Slitaz
Slitaz - 5.0 x64 - Firefox LibreOffice

```
|-------------------------------------------------------------------------------------|
|     ...                                                                    ...      |
|    (o-o)      Tuto SLITAZ 5.0 x64 VM WorkStation 12 by flo T2SI 2017      (o-o)     |
|ooO--(_)--Ooo                                                          ooO--(_)--Ooo |
|-------------------------------------------------------------------------------------|


   SSSSSSSSSSSSSSS lllllll                         TTTTTTTTTTTTTTTTTTTTTTT                                 
 SS:::::::::::::::Sl:::::l                         T:::::::::::::::::::::T                                 
S:::::SSSSSS::::::Sl:::::l                         T:::::::::::::::::::::T                                 
S:::::S     SSSSSSSl:::::l                         T:::::TT:::::::TT:::::T                                 
S:::::S             l::::lyyyyyyy           yyyyyyyTTTTTT  T:::::T  TTTTTTaaaaaaaaaaaaa   zzzzzzzzzzzzzzzzz
S:::::S             l::::l y:::::y         y:::::y         T:::::T        a::::::::::::a  z:::::::::::::::z
 S::::SSSS          l::::l  y:::::y       y:::::y          T:::::T        aaaaaaaaa:::::a z::::::::::::::z 
  SS::::::SSSSS     l::::l   y:::::y     y:::::y           T:::::T                 a::::a zzzzzzzz::::::z  
    SSS::::::::SS   l::::l    y:::::y   y:::::y            T:::::T          aaaaaaa:::::a       z::::::z   
       SSSSSS::::S  l::::l     y:::::y y:::::y             T:::::T        aa::::::::::::a      z::::::z    
            S:::::S l::::l      y:::::y:::::y              T:::::T       a::::aaaa::::::a     z::::::z     
            S:::::S l::::l       y:::::::::y               T:::::T      a::::a    a:::::a    z::::::z      
SSSSSSS     S:::::Sl::::::l       y:::::::y              TT:::::::TT    a::::a    a:::::a   z::::::zzzzzzzz
S::::::SSSSSS:::::Sl::::::l        y:::::y               T:::::::::T    a:::::aaaa::::::a  z::::::::::::::z
S:::::::::::::::SS l::::::l       y:::::y                T:::::::::T     a::::::::::aa:::az:::::::::::::::z
 SSSSSSSSSSSSSSS   llllllll      y:::::y                 TTTTTTTTTTT      aaaaaaaaaa  aaaazzzzzzzzzzzzzzzzz
                                y:::::y                                                                    
                               y:::::y                                                                     
                              y:::::y                                                                      
                             y:::::y                                                                       
                            yyyyyyy                                                                        


      .----------.                                                                                              _____      
     /          /                                                                                              /    /      
    /   ______.'                                                                                              /    /       
   /   /_                                                                                       .-''''-.     /    /        
  /      '''--.            .-''` ''-.                                                          /  .--.  \   /    /         
 '___          `.        .'          '.             ,.----------.             ____     _____  /  /    '-'  /    /  __      
     `'.         |      /              `           //            \           `.   \  .'    / /  /.--.     /    /  |  |     
        )        |     '                '          \\            /             `.  `'    .' /  ' _   \   /    '   |  |     
......-'        /,.--. |         .-.    |           `'----------'                '.    .'  /   .' )   | /    '----|  |---. 
\          _..'`//    \.        |   |   .                                        .'     `. |   (_.'   //          |  |   | 
 '------'''     \\    / .       '._.'  /                                       .'  .'`.   `.\       '  '----------|  |---' 
                 `'--'   '._         .'                                      .'   /    `.   `.`----'              |  |     
                            '-....-'`                                       '----'       '----'                  /____\    
```

SliTaz est un système GNU/Linux fournissant un bureau ou un serveur complet dans moins de 30Mb. SliTaz est distribuée sous forme de LiveCD, le système est (très) léger, rapide et simple à utiliser. SliTaz fournit un bureau graphique intuitif et élégant, le meilleur support matériel possible et dispose d'une communauté active

## --- Préparation de l'installation ---

###### - Télécharger l'ISO "Rolling" de Slitaz en version x64
	slitaz-rolling-core64.iso
	http://www.slitaz.org/fr/
	http://mirror.slitaz.org/iso/rolling/

###### - VMware Workstation / New Virtual Machine / Custom:
	-> Choisir "I will install the operating system later"
	-> Choisir "Linux" & "Other Linux 3.x Kernel 64-bit"
	-> Nommer & choisir l'emplacement de la VM
	-> Déterminer les paramètres processeur de la VM - (1 CPU - 4 Cores ?)
	-> Déterminer les paramètres mémoire de la VM - (2048 MB ?)
	-> Choisir "Use bridged networking"
	-> Choisir "LSI Logic" pour la selection I/O Controller
	-> Choisir "SATA" pour le type de disque
	-> Choisir "Create a new virtual disk"
	-> Determiner les paramètres du disque:
		-> Choisir la taille maxi du disque (12 GB ?)
		-> Cocher "Allocate all disk space now"
		-> Choisir "Store virtual disk as a single file"
	-> Modifier (éventuellement) le nom & l'emplacement du fichier disque
	-> Dans le récapitulatif: cliquer sur "Customize Hardware"
		-> Onglet "New CD/DVD":
			-> Choisir "Use ISO image file" et aller chercher l'iso de Slitaz (slitaz-rolling-core64.iso)
	-> Cliquer sur "Finish"
	-> Patienter pendant la création des fichiers.

## --- Installation de Slitaz ---

###### - Démarrer le live de Slitaz x64 en fr:
	-> Cliquer sur "Power on this virtual machine" et basculer dans la fenêtre de la VM
	-> au boot: allr dans "Languages" & choisir "Français" + [TAB] + [ENTER] pour valider
	-> [ENTER] pour lancer le live de Slitaz en fr
	-> Au login : root/root
	-> # tazx
	-> "Installer ou reconfigurer Xorg"
	-> Choisir le pilote Xorg "vmware"
	-> # startx
	-> Le Live de Slitaz x64 est démarré.

###### - Installation de Slitaz x64:
	-> Menu / Outils système / Tableau de bord Slitaz
	-> Installation / Installation / Installer Slitaz
	-> Lancer Gparted:
		-> Périphérique / Créer une table de partition
		-> Choisir msdos & valider
		-> Créer une première partition pour le SWAP (2048 Mio ?) & Système de fichiers "linux-swap"
		-> Créer une deuxième partition pour le système et le /home(taille max ?) & Système de fichiers "ext4"
		-> Valider la création des 2 partitions
		-> Gérer les drapeaux sur la 2ème partition et choisir "boot"
		-> Fermer Gparted
	-> Cliquer sur "Continuer l'installation"
		-> Média source de Sliaz: "Live CD"
		-> Installer Sliaz sur la partition en ext4 (sda2 ?)
		-> option de formattage: ext4
		-> Parition /home: laisser tel quel (ou ?)
		-> Définir le nom du système: laisser tel quel (ou ?)
		-> Mot de passe de l'administrateur Root: laisser tel quel (ou ?)
		[VM => Login "root" Pass "toor"]
		-> Identifiant de l'utilisateur: Laisser tel quel (ou ?)
		-> Mot de passe de l'utilisateur: laisser tel quel (ou ?)
		[VM => User Login "user1" Pass "totor"]
		-> Cocher "Installer un chargeur d'amorçage" (GRUB)
		-> Lancer l'installation de Slitaz
		-> Patienter puis fermer le TazPanel & éteindre le système.

###### - Premiers réglages & premier lancement:
	-> VMware Workstation / Edit virtual machine settings
	-> CD/DVD / "Use physical drive" sur Auto detect + [OK]
	-> 1er lancement: "Power on this virtual machine"
		-> [ENTER] dans GRUB pour valider
		-> slitaz login: en Root
		-> # tazx
		-> "Installer ou reconfigurer Xorg"
		-> Choisir le pilote Xorg "vmware"
		-> # startx
		-> Reboot
	-> Passage de Slitaz en fr (ou pas ?)
		-> se loguer en User
		-> Menu / Preferences / System language
		-> valider le login Root
		-> Choisir: "fr_FR@euro French locale for France with Euro"
		-> Reboot
		-> se loguer en User
		-> Touti ok ? Eteindre le système

## --- Installation des VM Tools ---

	-> VMware Workstation / Edit virtual machine settings
	-> Options / WMware Tools
	-> Choisir "Update automatically"
	-> Lancer la VM et se loguer en User
	-> Menu / Outils système / Terminal Sakura: (installation des paquets manquants)
		-> passer en Root: $ su / PassRoot / + # cd
		-> # tazpkg recharge
 		-> # tazpkg get-install slitaz-toolchain
		-> # tazpkg get-install ncurses-dev
		-> # tazpkg get-install perl
		-> # tazpkg search vmware
		-> # tazpkg get-install xorg-xf86-video-vmware --forced
		-> # tazpkg search vmmouse
		-> # tazpkg get-install
		-> # tazpkg get-install xorg-xf86-input-vmmouse
		-> # tazpkg search procps
		-> # tazpkg get-install procps
	-> Création des dossiers pour les VM Tools:
		-> # mkdir /etc/pam.d
		-> # mkdir /etc/init.d/rc0.d
		-> # mkdir /etc/init.d/rc1.d
		-> # mkdir /etc/init.d/rc2.d
		-> # mkdir /etc/init.d/rc3.d
		-> # mkdir /etc/init.d/rc4.d
		-> # mkdir /etc/init.d/rc5.d
		-> # mkdir /etc/init.d/rc6.d
		-> Quitter / fermer la console & Reboot
	-> Installation des VM Tools:
		-> Se loguer en User
		-> VMware Workstation: VM / Install VMware Tools
		-> Ouvrir le lecteur VMware Tools (/media/cdrom)
		-> Copier l'archive VMwareTools-XXX.tar.gz
		-> Coller l'archive dans le dossier Tmp (/tmp)
		-> Outils / Ouvrir le dossier actuel dans un teminal
		-> Passer en Root ($ su)
		-> # tar -xzvf VMwaretools.XXX.tar.gz
		-> # cd /tmp/vmware-tools-distrib/
		-> # ./vmware-install.pl -d
		-> Quitter / fermer la console & Reboot

<-------------------------------------------------------------------------------->
###### SI Problème VMware KB2147454

https://kb.vmware.com/selfservice/microsites/search.do?language=en_US&cmd=displayKC&externalId=2147454

	-> Reboot et se loguer en User
	-> VMware Workstation / VM / Reinstall VMware Tools
	-> Ouvrir le media VMware Tools (/media/cdrom)
	-> Copier tout & coller le tout dans le dossier Tmp
	-> Editer avec Beaver le script "run_upgrade.sh" pour voir si le script commence par #!/bin/bash
	-> Si oui alors: console en Root
	-> # tazpkg -gi bash
	-> Reboot (?)
	-> Lancer le script "run_upgrade.sh": console en Root:
	-> # chmod +x /tmp/run_upgrade.sh
	-> Reboot (?)
	-> VMware Workstation / VM / Reinstall VMTools / Copier/Coller Tar.Gz dans /tmp
	-> console en Root:
	-> # tar ...
	-> # cd ...
	-> # ./vmware-....pl.d
<-------------------------------------------------------------------------------->

###### 	-> Verification des paramètres:
		-> se loguer en User
		-> Ouvrir une console Sakura / su / # cd
		-> # cd /etc/X11/
		-> # ls
		-> # cd xorg.conf.d/
		-> # ls
		-> # nano 60-Device.conf
		-> Verifier que pour "Card0" le Driver est bien "vmware" (sinon corriger) ([ctrl]+[X]...) 
		-> # cat 50-vmmouse.conf
		-> Vérifier que le Driver de la souris est bien "vmmouse" (sinon corriger avec nano)
		-> # cd
		-> # nano /etc/rcS.conf
		-> vers la fin du fichier / section "RUN_DAEMONS="
		-> Ajouter apres ntpd: vmware-tools (sans casser les "...)
		-> Quitter fermer la console & Reboot
	-> Validation des VM Tools:
		-> Se loguer en User
		-> Lancer une console Sakura / su / # cd
		-> # /etc/init.d/vmware-tools status
		-> Vérifier que les service vmtoolsd est actif
		-> Quitter fermer la console
		-> Régler vos paramètres écran: Menu / Préférences / Paramètres de l'écran
		-> Reboot
		-> Check
		-> Eteindre la VM & SnapShot !


###### Enjoy ! Slitaz 5.0 x64 est installé en VM avec les Tools !
###### Bons Clics...



```

|-------------------------------------------------------------------------------------|                          
|     ...                                                                    ...      |             
|    (o-o)      Tuto SLITAZ 5.0 x64 VM WorkStation 12 by flo T2SI 2017      (o-o)     |              
|ooO--(_)--Ooo          Installation Firefox - LibreOffice              ooO--(_)--Ooo |
|-------------------------------------------------------------------------------------|


.................######..##.......####.########....###....########...............
................##....##.##........##.....##......##.##........##................
................##.......##........##.....##.....##...##......##.................
.................######..##........##.....##....##.....##....##..................
......................##.##........##.....##....#########...##...................
................##....##.##........##.....##....##.....##..##....................
.................######..########.####....##....##.....##.########...............


#######                                                  #                              #######                               
#       # #####  ###### ######  ####  #    #             #       # #####  #####  ###### #     # ###### ###### #  ####  ###### 
#       # #    # #      #      #    #  #  #              #       # #    # #    # #      #     # #      #      # #    # #      
#####   # #    # #####  #####  #    #   ##      #####    #       # #####  #    # #####  #     # #####  #####  # #      #####  
#       # #####  #      #      #    #   ##               #       # #    # #####  #      #     # #      #      # #      #      
#       # #   #  #      #      #    #  #  #              #       # #    # #   #  #      #     # #      #      # #    # #      
#       # #    # ###### #       ####  #    #             ####### # #####  #    # ###### ####### #      #      #  ####  ###### 

```
## --- Installation de Firefox & LibreOffice ---

###### - Installation de Firefox:
	-> Démarrer la VM et se loguer en User
	-> Ouvrir une console Sakura et passer en SU
	-> # tazpkg search firefox
	-> # tazpkg get-install firefox-official-fr (v51 ou + ?)
	-> Lancer Firefox / paramétrer Firefox
	-> Valider les mise à jour Firefox jusu'à ce qu'il soit à jour
	-> Lancer Firefox via le raccourcis du Menu, si touti ok, commencer à l'utiliser...

###### - Installation de LibreOffice:
	-> Démarer la VM et se loguer en User
	-> Ouvrir une console Sakura et passer en SU
	-> Installation de IcedTea (JAVA Alternative...)
		-> # tazpkg search icedtea
		-> # tazpkg get-install icedtea6-jdk
		-> Reboot
	-> Installation de LibreOffice
		-> Ouvrir une console Sakura et passer en SU
		-> # tazpkg search libreoffice
		-> # tazpkg get-install get-LibreOffice
		-> # get-LibreOffice (it's time to have a break...)
		-> Reboot
	-> Validation de l'installation de LibreOffice (correction d'un lien symbolique)
		-> Ouvrir une console Sakura et passer en SU
		-> # cd /usr/bin
		-> # ln -sfn /usr/lib/libreoffice5.4/program/soffice ./libreoffice5.4
		-> Reboot
	-> Premier lancement de LibreOffice
		-> Se loguer en User
		-> Ouvrir une console Sakura
		-> $ soffice
		-> Outils / Options / LibreOffice / Avancé
		-> Vérifier que l'option "utiliser un environnement d'exécution Java" est activée
		-> Et qu'un moteur Java est selectionné.
		-> Fermer l'application LibreOffice
		-> Démarrer une application LibreOffice via les raccourcis du Menu
		-> Si touti ok, commencer à utiliser LibreOffice...

###### Enjoy !
###### Bons Clics...
