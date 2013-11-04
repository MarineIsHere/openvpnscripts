OPENVPN AUTO-INSTALLER FOR OPENVZ / PROXMOX 3 (not tested on Proxmox 2) USE !<br />
Installeur OpenVPN pour un usage avec OpenVZ / Proxmox 3 (non testé sous Proxmox 2) !<br />
<br />
<h4>--- FRENCH / FRANCAIS ---</h4>

pour installer entrez ces commande en root (sudo su root)<br />
script compatible OpenVZ / Proxmox 3 avec Containeur sous Debian (6 & 7), Ubuntu (12.04) ou CentOS (5 & 6)

installer les packets git et dos2unix :

DEBIAN/UBUNTU : <b>apt-get -y install git dos2unix</b>
CENTOS : <b>yum -y install git dos2unix</b>

<b>cd /tmp && git clone git://github.com/nicolargo/openvpnscripts.git && dos2unix openvpnscripts/install.sh && chmod +x openvpnscripts/install.sh  && openvpnscripts/install.sh
</b>
après installation pour crée un client executez ovcreateclient nom du client :<br />
<b>ovcreateclient nom_du_client</b>

vous pouvez ensuite récupérer l'archive zip dans le dossier /etc/openvpn/clientconf/nomduclient
<br />
<br />
<h4>--- ENGLISH / ANGLAIS ---</h4>

for install enter commande in root (sudo su root)<br />
script compatibility for OpenVZ using Proxmox 3 or no. VZ running Debian (6 & 7), Ubuntu (12.04) or CentOS (5 & 6).

install packets git and dos2unix :

DEBIAN/UBUNTU : <b>apt-get -y install git dos2unix</b>
CENTOS : <b>yum -y install git dos2unix</b>

<b>cd /tmp && git clone git://github.com/nicolargo/openvpnscripts.git && dos2unix openvpnscripts/install.sh && chmod +x openvpnscripts/install.sh  && openvpnscripts/install.sh
</b>
after install for create client execute ovcreateclient name of client :<br />
<b>ovcreateclient user_name</b>

you can then retrieve the zip file in the /etc/openvpn/clientconf/nameofclient
