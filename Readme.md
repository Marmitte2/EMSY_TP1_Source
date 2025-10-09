# TP1 - Installation Linux sur une VM - V0.1

## Groupe 

Valentin Mermoud / Loïc Marmy

## But 

Cette manipulation a pour but d'installer une distribution linux [Sparky Linux](https://sparkylinux.org/) dans une machine virtuelle VMware Workstation Player, à l’aide d’une image disque (ISO).

## Materiels à disposition 

- VMware Workstation Player - V17
- Image disque (ISO) : sparkylinux-6.4-x86_64-minimalcli.iso

## Utilisation de VMware et de l'image ISO linux 

A. Lancez VMware Workstation Player (logiciel)  

B. Sélectionnez **Create a New Virtual Machine** 

C. Placez le fichier `.iso` dans une repertoire connu : 

`C:\VosInitiales\VM\ISO`

D. Indiquez le chemin d’accès de l’image iso comme indiqué sous l’image ci-dessous :

![install image disk](/Images/Install_ISO.jpg) 

E. Choisir un nom d'OS : `Linux - Debian 11.x` 

![OS name choice](/Images/OS_Choice.jpg) 

F. Nommez la machine virtuelle : `SparkyLinux-VosInitiales` 

G. Creez un disque virtuel -> capcité : **20GB** 

> remarque$$^1$$ : cocher **store virtual disk a single file**

![Virtual disk](/Images/VirtualDisk.jpg) 

> remarque$$^2$$ : ci-dessous, la configuration de la VM 

![Virtual disk](/Images/VM_Config.jpg) 

H. Lancez la machine virtuelle : **Play virtual machine** 

## Lancement de l'image ISO (Linux - Live CD) 

G. Lancement du live CD : 

<img width="813" height="662" alt="image" src="https://github.com/user-attachments/assets/7d18aea7-7ad6-42b2-b9d4-471165c5474e" />
 
Shell Linux : 

[Placer votre capture d'écran]() 

> **ATTENTION** : par défaut, le clavier est configuré est **Clavier Americain**

Q1. disposition du clavier américain ?

> QWERTY

Q2. disposition du clavier suisse-romand ?

> QWERTZ

Q3. disposition du le clavier français ? 

> AZERTY

H. Déplacez-vous à la **racine du système** en utilisant la commande suivante : `cd` 

> cd /

I. Affichez le contenu de la racine avec la commande : `ls –l`	

<img width="803" height="656" alt="image" src="https://github.com/user-attachments/assets/aecdec4a-8416-4f9a-b5f1-21c2f595f085" />

Q5. Que signifie l'option `-l` avec la commande `ls` 

> le -l est pour avoir un format long et detaillé d'une commande 

Q6. Décrypter la ligne où se trouve le répertoire **home**    

<img width="799" height="654" alt="image" src="https://github.com/user-attachments/assets/c960c031-f0d8-4d5d-923e-6e1357b0a043" />

J. Créez un répertoire de travail nommé « EMSY_VosInitiales» dans quel dossier racine allez-vous le placer (justifiez votre réponse) et quelle commande allez-vous utiliser. 

> dans le repertoire home/live/ car c'est le repertoire utilisateur.
avec la commande mkdir

Q7. Si vous créez un répertoire de travail (pour éditer/sauvegarder des fichiers), dans quelle **répertoire racine** vous vous placez ? 

> dans le home/live/ car c'est le repertoire utilisateur


K. Dans ce répertoire, créez un fichier texte que vous nommerez `TESTSLO_XXX_XXX` et éditez celui en écrivant un texte, exemple : "TP linux by XXX et XXX".
	Utiliser la commande `vi`

> vi TESTSLO_VMD_LMY

Q9. dans le répertoire `/home`, pouvez-vous éditez un fichier uniquement avec la commande `vi` 

> Oui on peut ouvrir l'éditeur et donc éditer un fichier

Q10. Si vous éteignez la machine virtuelle et que vous la rallumez, est-ce que le répertoire créé ci-dessus existe toujours (justifiez votre réponse) ? 

> Non le répertoire n'existe plus 

L. Tapez la commande `ls -l /dev/sda` 

<img width="797" height="656" alt="image" src="https://github.com/user-attachments/assets/864f816d-16b6-4b88-af31-8839c59b4c58" />

Q11. Que signifie **sda** ? 

> C'est le premier disque dur reconnu par linux

Q12. Décrypter la réponse après avoir taper la commande `ls -l /dev/sda` -> voir résultat point 13.

> <img width="793" height="646" alt="image" src="https://github.com/user-attachments/assets/808afafa-0065-4503-b550-01845841c13e" />

Q13. Quelle est la taille du disque minimum recommandé pour installer la distribution sparky ?

> 512MB

Q14. A quoi sert la partition swap ? Est ce que ce principe existe sur les OS Microsoft Windows ?

> C'est une RAM additionnelle, non windows n'utilise pas des partion swap cependant windows utilise des fichiers d'échange dans le disque C quand la RAM est saturée

Q.15 Quel format pourriez-vous utiliser pour la 3ème partition afin qu'elle soit également accessible depuis un OS Microsoft ?

> W95 FA32

Q.16 Durant l'installation, on vous demande deux nom d'utilisateur. A quoi correspondent-ils?

>
N. Après l'installation de linux, prenez une capture d'écran du démarrage de votre système (grub)

> <img width="639" height="532" alt="image" src="https://github.com/user-attachments/assets/173cb682-79fd-4d12-a801-0eab29b50b7f" />

O. Trouvez la ou les lignes de commande permettant de changer le clavier(clavier suisse romand trouvable sous <<german (switzerland)) et procédez à la configuration du clavier.

> sudo nano /etc/default/keyboard --> XKBLAYOUT="ch"XKBVARIANT="de"

P. Testez si l’application « nano » est installée sur votre machine, tapez la commande : 
nano --version
Q17. À quoi sert « nano » ?

> nano est un éditeur de texte dans le ternimal qu'on peut utiliser pour éditer facilement des fichiers de configuration

Q. Testez si l’application « git » est installée sur votre distribution, si ce n’est pas le cas installez
un client git.
Q18. Comment savoir si « git » est déjà installé ? 

> il faut taper la commande git --version et si on ne trouve rien c'est que git n'est pas installée

Q19. Quelle(s) commande(s) utilisez-vous pour l’installer ? 

> sudo apt install gity

Q20. Que veut dire « apt » ? 

> apt = advanced package tool qui est un outil de gestion de paquet

Q21. Est-ce que cette commande peut être utilisée sur toutes les distributions Linux ?

> Elle n'est pas utilisable sur toutes les plateformes parce que les différentes distribution Linux ont étées faites avec des philosophies différentes

R. Créez un sous-répertoire « EMSY_TP1_XXX-YYY » dans le répertoire de votre utilisateur.
Attention : Ici on veut que l’utilisateur (vous) ait les droits de lecture, d’écriture et d’exécution.
Q22. Quel est le répertoire utilisateur ?

> home/"repertoire utilisateur"

Q23. Quelles sont les commandes que vous allez utiliser ?

> cd home/lmy --> mkdir EMSY_TP1_VMD-LMY

S. Dans ce répertoire, tapez la commande : 
git clone https://github.com/votreDepot/EMSY_TP1_Source
Il faut au préalable que vous ayez mis en place à cette adresse un fork du dépôt fourni.
Q24. Qu’observez-vous dans votre répertoire ?

> On y retrouve notre répertoire du EMSY_TP1

T. Editez le fichier source .c avec l’éditeur de texte « nano ».
Réalisez un petit programme en C (par exemple de type « Hello world »).


## Tips 

> $$Tips^1$$ : sortir de la VM -> appuyer simultanément sur `Ctrl` et `Alt` 

> $$Tips^2$$ : arrêter la VM proprement -> commande : `shutdown`

> $$Tips^3$$ : arrêter la VM pour cause de plantage -> commande : `halt` ou `poweroff`

> $$Tips^4$$ : [commande vi avec ses options](https://www.linuxtricks.fr/wiki/guide-de-sur-vi-utilisation-de-vi)

> $$Tips^5$$ : [éditer un fichier type markdown (.md)](https://ashki23.github.io/markdown-latex.html)

