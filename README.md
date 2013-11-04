OPENVPN AUTO-INSTALLER FOR OPENVZ / PROXMOX 3 (not tested on Proxmox 2) USE !<br />
Installeur OpenVPN pour un usage avec OpenVZ / Proxmox 3 (non testé sous Proxmox 2) !<br />
<br />
<h4>--- FRENCH / FRANCAIS ---</h4>

Vous devez exécuter les commande suivante sur l'hôte Proxmox, en tant que root (pensez à remplacer VM_ID par l'ID de votre CT OpenVPN !) : <br />
<b>vzctl set <u>VM_ID</u> --iptables iptable_filter --iptables ipt_length --iptables ipt_limit --iptables iptable_mangle --iptables iptable_nat --save</b>
<br />
<br /><b>Arrêtez votre VM</b>
<br />CTID=<u>VM_ID</u>
<br />vzctl set $CTID --devnodes net/tun:rw --save
<br />vzctl set $CTID --devices c:10:200:rw --save
<br />vzctl set $CTID --capability net_admin:on --save
<br />vzctl exec $CTID mkdir -p /dev/net
<br /><b>Démarrez votre VM</b>
<br />vzctl exec $CTID mknod /dev/net/tun c 10 200
<br />vzctl exec $CTID chmod 600 /dev/net/tun

Rendez-vous sur le SSH de votre VM OpenVPN. Pour installer OpenVPN, entrez ces commande en root (sudo su root)<br />
script compatible OpenVZ / Proxmox 3 avec Containeur sous Debian (6 & 7), Ubuntu (12.04) ou CentOS (5 & 6)

installer les packets git et dos2unix :

DEBIAN/UBUNTU : <b>apt-get -y install git dos2unix</b>
<br />CENTOS : <b>yum -y install git dos2unix</b>

<b>cd /tmp && git clone git://github.com/o-be-one/openvpnscripts.git && dos2unix openvpnscripts/install.sh && chmod +x openvpnscripts/install.sh  && openvpnscripts/install.sh
</b>
après installation pour crée un client executez ovcreateclient nom du client :<br />
<b>ovcreateclient nom_du_client</b>

vous pouvez ensuite récupérer l'archive zip dans le dossier /etc/openvpn/clientconf/nomduclient
<br />
<br />
<h4>--- ENGLISH / ANGLAIS ---</h4>

You must execute the following command on your Proxmox host as root (don't forget to replace VM_ID by your OpenVPN VZ ID)<br />
<b>vzctl set <u>VM_ID</u> --iptables iptable_filter --iptables ipt_length --iptables ipt_limit --iptables iptable_mangle --iptables iptable_nat --save</b>
<br />
<br /><b>Stop your VM</b>
<br />CTID=<u>VM_ID</u>
<br />vzctl set $CTID --devnodes net/tun:rw --save
<br />vzctl set $CTID --devices c:10:200:rw --save
<br />vzctl set $CTID --capability net_admin:on --save
<br />vzctl exec $CTID mkdir -p /dev/net
<br /><b>Start your VM</b>
<br />vzctl exec $CTID mknod /dev/net/tun c 10 200
<br />vzctl exec $CTID chmod 600 /dev/net/tun

Rendez-vous sur le SSH de votre VM OpenVPN. Pour installer OpenVPN, enter commande in root (sudo su root)<br />
script compatibility for OpenVZ using Proxmox 3 or no. VZ running Debian (6 & 7), Ubuntu (12.04) or CentOS (5 & 6).

install packets git and dos2unix :

DEBIAN/UBUNTU : <b>apt-get -y install git dos2unix</b>
<br />CENTOS : <b>yum -y install git dos2unix</b>

<b>cd /tmp && git clone git://github.com/o-be-one/openvpnscripts.git && dos2unix openvpnscripts/install.sh && chmod +x openvpnscripts/install.sh  && openvpnscripts/install.sh
</b>
after install for create client execute ovcreateclient name of client :<br />
<b>ovcreateclient user_name</b>

you can then retrieve the zip file in the /etc/openvpn/clientconf/nameofclient
