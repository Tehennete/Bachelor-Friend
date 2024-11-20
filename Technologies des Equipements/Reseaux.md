---
aliases: 
Matière:
  - Technologie des Equipements
Semestre:
  - B3-1
Date: 2024-10-17
Prof: "[[Philippe Domengie]]"
Type: notes de cours
tags:
  - cours
  - Technologie-des-équipements
---
# Réseau 
Date: [[2024-10-17]]

### Intro 
Toute machine communique à travers le réseau… 

## Couches de réseau
Deux modeles : Complexe = OSI / Plus simple = DoD 
Données qui rentrent arrivent par le bas et données qui sont transmises partent depuis l'application. 
(Cf C.1.1)
### Couche accès réseau 
D'où le nom de la couche qui accueille les données = Accès réseau / Physique.
Types de protocol d'accès réseaux > donnée cellulaires (3g,4g,5g) Fttth (Fibre), ethernet, wifi. 
Le termes protocol englobe le type de support physique, 

La couche accès réseau s'occupe d'adapter les données pour les mettre partager sur le support physique ou de les extraire vers des données utilisable. 

### Couche internet  / IP 
Par abus de language, nommée IP car le protocole le plus utilisé dans cet couche est l'**Internet Protocol**

Le but de cette couche est d'attribuer des adresses à chacune des machines connectées au réseaux. 
Quand on communique à travers le réseaux il y a forcément deux adresses utilisées, l'émetteur et le récepteur. 

### Couches transport 
Elle s'occupe quand on envoie des infos : Elle découpe les données en paquets de taille égale. 
Et elle reassemble les paquets dans l'autre sens 
Ce decoupage est valable pour tous les types de protocoles de transport. 
#### TCP 

Cela permet d'éviter la perte de données, car comme ils sont numérotés, la machine destinataire peut demander un nouvel envoie des paquets qui ne sont pas arrivée. 
Et chaque paquet fait parti d'une somme de control. 
Cette somme de contrôle est tamponnée sur chaque paquet, du coup cela permet de verifier le paquet car si ce n'est pas la meme somme le paquet n'est pas le meme. 

Avantage : Tu es sur que ce que tu reçois est identique à ce que tu as envoyé. 
Desavantage : On ne peut pas lire le fichier pendant le transfert 
#### UDP
On ne peut pas utiliser ce système dans une transmission en streaming. On utilise l'UDP, sans checksum (Somme de contrôle). Ici tout est fluide sauf si il y a un soucis sur la connexion. → Les paquets n'arrive plus au bon rythme, donc roue qui tourne. 

>[!note]
>On appel le réseau en TCP/ IP car la couche TCP est au dessus de la couche IP. Or pour du Dantes c'est bien le protocol UDP (car Live/direct) 

Protocole de transport pour la video RTP…. 


### Couche application
Elle est chargée de mettre a disposition des applications ce qui arrive du réseau 
Ou de mettre dans le réseaux les informations issues des applications. 

Il a y a des protocoles qui vont preparer les données pour leur entrée dans le réseau
Il y a des protocols de partage de fichiers entre machines… 
Ex : HTTP, FTP, NFS

Chacun des protocole est associé à un port et un socket. Donc ils ont tous un numéro de port. 
Cela permet de tamponner les données empaquetées avec le port. Pour que les applications puissent analyser les paquets qui les intéresse 

Port 80 pour le protocole http par exemple 

Il y a des protocoles qui envoient des paquets réguliers → Comme l'heure 

Le dantes est un protocole qui rassemble plusieurs 
Il y a le transport UDP et des protocols de synchronisation des signaux et un protocol de plus basse couche, qui est un protocol de QoS quality of service qui permet de donner la priorité aux différents signaux. (Le signal de synchro est plus interessant que le signal audio.)

## L'Internet Protocol 
### Écriture d'une adresse IP
Ecriture d’une adresse IP
256 possibilités de coder en 8 bits (2^8) 4 nombres donc 32 bits.
Exemple : de 0.0.0.0 à 255.255.255.255 => 256x256x256x256 = environ 4 milliards de possibilités (2^32). C’est l’IPv4 (4 nombres).
On en est à la 6ème version de l’IP (IPv6). L’adresse est donc beaucoup plus longue et exprimée en hexadécimal.

On a 2 gammes d’adresses IP :
Publiques = en dehors des réseaux privés. C’est l’internet
Privées = LAN (exemple WIFI d’un aéroport ou le sien). Elles sont du type 192.168.x.x ( et on peut changer)
Routeur : permet d’aiguiller les paquets d’un réseau à un autre (exemple : d’un LAN à internet). Chez soi, c’est la box internet qui assume ce rôle.


#### NAT (Network Adress Translation)
C’est un protocole qui permet de changer une adresse IP privée en publique. Cela permet d’envoyer un fichier d’un ordinateur sur internet par exemple.

(  VPN : on crée une autre adresse publique différente de la sienne et on y ajoute un cryptage.
SSID : nom du réseau WIFI  )

#### DHCP (Dynamic Host Configuration Protocol)
Ce protocole attribue une adresse IP automatiquement à chaque personne qui se connecte à un réseau public en utilisant les adresses MAC. Il est utilisé sur les réseaux publics comme privés.
Chez soi, c’est la box qui fait ‘tourner’ le DHCP. Une box fonctionne grâce à un Linux embarqué d’ailleurs, lui permettant de faire du DHCP, NAT, etc.
Le DHCP attribue une adresse IP pour une durée limitée : c’est le bail. Il dure 24h (84600s) et est renouvelable.
Il existe le DHCP fixe : il attribue les adresse IP mais mémorise certaines adresses IP.
Adresse MAC : Media Access Control. Elle est composée de 5 nombres hexadécimaux.

>[!note] 
>WAN : Wide Area Network
LAN : Local Area Network
WLAN : LAN déployé par le WIFI (Wireless LAN)

Pour se connecter à sa box, rentre son adresse IP. Cela permet de voir le DHCP (avec adresse IP et MAC associées).

**Plage d'adresses privées autorisées :** 
Class A : 10.0.0.0 - 10. 255.255.255
Class B : 172.16.0.0 - 172. 31.255.255
Class C : 192.168.0.0 - 192.168.255.255

### Les classes de réseau 
Permet de determiner la partie de l'adresse IP dans ce reseau qui sera en commun sur toutes les machines et quelle partie de l'IP sera celle qui varie sur les machines. 
#### Class A 
Premier 8 bits qui sont communs à tous. Donc 16M de machines différentes. 
Donc tres peu utilisé 

#### Class B 
Deux premiers nombres qui seront en commun pour un meme réseau. 
On peut faire différents reseau sur un meme lan avec chaque réseau qui aura sont 2ème digits de 16 à 32. → Soit 16 réseaux de class B possible. 

#### Class C
Deux premier nombre = commun 
Troisième permet de faire différents  réseaux ici 254
Quatrième pour différencier chaque machine. 254 

Il y a deux adresses que l'on ne peut pas donner aux machines : C'est la premiere qui definit le reseau. 
Et la dernière : l'adresse broadcast 

#### Exemples 
**Class A** 
10.0.0.0 = adresse reseau class A
1er ad dispo = 10.0.0.1
Dernière ad dispo = 10.255.255.254
Ad broadcast = 10.255.255.255 
**Class B** 
172.20.0.0 → Adresse reseau 172.28.0.0 (adresse d'un autre reseau sur le meme lan)
1er ad dispo = 172.20.0.1
Der ad dispo = 172.20.255.254
Ad broadcast = 172.20.255.255
**Class C**
192.168.113.0 → Adresse reseau 172.28.0.0 (adresse d'un autre reseau sur le meme lan)
1er ad dispo = 192.168.113.1
Der ad dispo = 192.168.113.254
Ad broadcast = 192.168.113.255
### Masques de reseau 
Le masque de sous reseau permet d'indiquer la class de reseau. 
255 → donne les bits attribués au reseau
0 → donne les bits attribués au machines. 

>[!note]
>**Masque sous reseau** 
>Class A : 255.0.0.0 → CIDR/ 8
>Class B : 255.255.0.0 → CIDR/16
>Class C : 255.255.255.0 → CIDR/24

#### Notation en CIDR 
Donne le nombre de bits 1 terminant l'adresse 
CIDR/8 = 255.0.0.0 → 1111 1111.0000 0000.0000 0000.0000 0000
CIDR/16 = 255.255.0.0 → 1111 1111.1111 1111.0000 0000.0000 0000
CIDR/24 = 255.255.255.0 → 1111 1111.1111 1111.1111 1111.0000 0000


Masque de sous reseau or 8 - 16 - 24
On veut pouvoir limiter un reseau car pas besoin de 256 adresses. On peut donc faire un masque different. 
Binaire  : 1111 1111.1111 1111.1111 1111.1110 000
Décimale : 255.255.255.224
CIDR = 27
Il reste 5 bits pour adresser les machines, donc 32 en décimale. ce qui nous donne la valeur du masque → 256-32 = 224

Si on choisit comme adresse reseau: 192.168.0.0/27, la dernière adresse sera donc 192.169.0.31 → Adresse broadcast 
Donc il y aura 30 adresses disponible 