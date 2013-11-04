OPENVPN AUTO-INSTALLER FOR OPENVZ / PROXMOX 3 (not tested on Proxmox 2) USE !
Installeur OpenVPN pour un usage avec OpenVZ / Proxmox 3 (non testé sous Proxmox 2) !


--- FRENCH / FRANCAIS ---

pour installer entrez ces commande en root (sudo su root)
script compatible OpenVZ / Proxmox 3 avec Containeur sous Debian (6 & 7), Ubuntu (12.04) ou CentOS (5 & 6)

installer les packets git et dos2unix :

apt-get -y install git dos2unix or (ou) yum -y install git dos2unix
cd /tmp && git clone git://github.com/nicolargo/openvpnscripts.git && dos2unix openvpnscripts/install.sh && chmod +x openvpnscripts/install.sh  && openvpnscripts/install.sh

après installation pour crée un client executer ovcreateclient nom du client :
ovcreateclient <nom_du_client>

vous pouvez ensuite récupérer l'archive zip dans le dossier /etc/openvpn/clientconf/nomduclient



--- ENGLISH / ANGLAIS ---

for install enter commande in root (sudo su root)
script compatibility for OpenVZ using Proxmox 3 or no. VZ running Debian (6 & 7), Ubuntu (12.04) or CentOS (5 & 6).

install packets git and dos2unix :

apt-get -y install git dos2unix or (ou) yum -y install git dos2unix
cd /tmp && git clone git://github.com/nicolargo/openvpnscripts.git && dos2unix openvpnscripts/install.sh && chmod +x openvpnscripts/install.sh  && openvpnscripts/install.sh

after install for create client execute ovcreateclient name of client :
ovcreateclient <user_name>

you can then retrieve the zip file in the /etc/openvpn/clientconf/nameofclient
