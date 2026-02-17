# Projet_NAC

### Installation PacketFence
- VM avec 2 interfaces réseau :
  1. LAN interne (eth0)
  2. NAT (eth1)
- Configuration IP statique LAN
- Accès interface web : https://IP:1443
- Configuration du DNS vers AD
### Configuration Active Directory
- Installation AD DS
- Création domaine : nac.corp
- Installation DNS
- Installation NPS
- Ajout PacketFence comme client RADIUS
- Création Network Policy :
  1. PEAP
  2. MSCHAPv2
- Autorisation groupe utilisateurs
### Intégration LDAP dans PacketFence
Authentication Sources → LDAP
Paramètres :
Host : 192.168.1.2
Port : 389
Base DN : DC=nac,DC=local
Test LDAP → Bind successful ✅
### Configuration Client Windows 10
Activation IEEE 802.1X
Méthode : PEAP
### Scénarios de Test Réalisés
user1	✅ Access-Accept
user2	❌ Access-Reject
