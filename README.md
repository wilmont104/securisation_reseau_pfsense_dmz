# Sécurisation d’un réseau avec double pare-feu et DMZ (pfSense)

Ce projet présente la mise en place d’une architecture réseau sécurisée
basée sur le principe de la **défense en profondeur**, en utilisant deux
pare-feu **pfSense** afin d’isoler une **DMZ** du réseau interne (LAN)
et d’Internet (WAN).

Projet personnel réalisé dans le cadre de ma Licence
Administration Réseaux & Multimédia.

---

## 🎯 Objectifs du projet
- Sécuriser l’accès au réseau interne
- Isoler les services exposés dans une DMZ
- Mettre en œuvre un double pare-feu
- Appliquer des règles de filtrage réseau strictes
- Tester l’accessibilité et la sécurité des services

---

## 🏗️ Architecture réseau
L’architecture repose sur trois zones distinctes :
- **WAN** : accès Internet
- **DMZ** : serveurs Web et FTP
- **LAN** : utilisateurs internes et serveur AD/DNS

Deux pare-feu pfSense assurent la segmentation et le filtrage des flux :
- pfSense externe : WAN ↔ DMZ
- pfSense interne : DMZ ↔ LAN

---

## 🛠️ Environnement technique
- Pare-feu : pfSense
- Virtualisation : VMware / GNS3
- Systèmes :
  - Windows Server 2016 (AD, DNS, Web, FTP)
  - Windows 10 (clients)
- Services déployés :
  - Web (IIS)
  - FTP
  - Active Directory & DNS
  - Portail captif
  - NAT / Port forwarding

---

## 🔐 Principes de sécurité appliqués
- Segmentation réseau (WAN / DMZ / LAN)
- Défense en profondeur avec double pare-feu
- Blocage des accès directs WAN → LAN
- Accès WAN → DMZ limité aux ports nécessaires
- Contrôle des flux entre LAN et DMZ
- Utilisation du NAT pour l’exposition des services

---

## ✅ Résultats obtenus
- Les services Web et FTP sont accessibles depuis Internet via la DMZ
- Le réseau LAN est isolé et protégé
- Les flux non autorisés sont bloqués par les pare-feu
- Les communications internes et externes sont maîtrisées

---

## 📄 Documentation détaillée
La réalisation complète du projet (schéma réseau, plan d’adressage,
configuration des pare-feu, règles de filtrage, tests et analyse)
est disponible dans le document suivant :

👉 **[Voir le rapport détaillé du projet (PDF)](securité_pare-feu_dmz.pdf)**

---

## 📌 Statut du projet
Projet finalisé – améliorations possibles :
- IDS / IPS (Snort, Suricata)
- VPN client-to-site
- Authentification centralisée (LDAP)
- Chiffrement HTTPS

---

## 👤 Auteur
**SONTIA MBONING GABY WILONE**  
Étudiant en Licence – Administration Réseaux & Multimédia
