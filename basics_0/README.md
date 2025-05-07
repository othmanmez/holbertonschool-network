# Network Basics

Ce projet couvre les concepts fondamentaux des réseaux informatiques, notamment le modèle OSI, les types de réseaux, les adresses MAC et IP, ainsi que les protocoles TCP/UDP.

## Structure du Projet

### Fichiers de Réponses
- `0-OSI_model` : Réponses sur le modèle OSI
- `1-types_of_network` : Réponses sur les types de réseaux (LAN, WAN, Internet)
- `2-MAC_and_IP_address` : Réponses sur les adresses MAC et IP
- `3-UDP_and_TCP` : Réponses sur les protocoles UDP et TCP

### Scripts
- `4-TCP_and_UDP_ports` : Script qui affiche les ports TCP et UDP en écoute
  - Utilise la commande `netstat -tulpn`
  - Affiche les sockets en écoute avec leurs PIDs et noms de programmes

- `5-is_the_host_on_the_network` : Script qui vérifie si un hôte est sur le réseau
  - Prend une adresse IP en argument
  - Effectue 5 pings vers l'adresse IP spécifiée
  - Affiche les statistiques de ping

## Utilisation

### Pour afficher les ports en écoute :
```bash
sudo ./4-TCP_and_UDP_ports
```

### Pour vérifier si un hôte est sur le réseau :
```bash
./5-is_the_host_on_the_network 8.8.8.8
```

## Concepts Clés

1. **Modèle OSI**
   - Modèle conceptuel à 7 couches
   - Organisé du niveau le plus bas (physique) au plus haut (application)

2. **Types de Réseaux**
   - LAN (Local Area Network)
   - WAN (Wide Area Network)
   - Internet

3. **Adresses**
   - MAC : Identifiant unique d'une interface réseau
   - IP : Adresse logique pour identifier un périphérique sur un réseau

4. **Protocoles de Transport**
   - TCP : Transfert fiable mais plus lent
   - UDP : Transfert rapide mais sans garantie de livraison

5. **Ports Importants**
   - 22 : SSH
   - 80 : HTTP
   - 443 : HTTPS 