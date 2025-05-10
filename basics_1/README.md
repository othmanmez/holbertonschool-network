# Configuration Réseau

Ce projet contient des scripts pour la configuration et la gestion des réseaux sur un système Ubuntu.

## Scripts

### 0-change_your_home_IP
Script qui modifie le fichier `/etc/hosts` pour changer les résolutions DNS :
- `localhost` pointe vers `127.0.0.2`
- `facebook.com` pointe vers `8.8.8.8`

**Attention** : Ce script modifie les résolutions DNS système. Une sauvegarde du fichier hosts original est créée dans `/etc/hosts.bak`.

### 1-show_attached_IPs
Script qui affiche toutes les adresses IPv4 actives sur la machine :
- Utilise la commande `ip addr show`
- Filtre pour n'afficher que les adresses IPv4
- Affiche une adresse par ligne

Exemple de sortie :
```
10.0.2.15
127.0.0.1
```

### 2-port_listening_on_localhost
Script qui crée un serveur d'écoute sur le port 98 de localhost :
- Utilise netcat (`nc`) pour écouter sur le port 98
- Se limite à l'interface localhost (127.0.0.1)
- Permet de recevoir du texte envoyé via telnet

## Utilisation

### Pour modifier les résolutions DNS :
```bash
sudo ./0-change_your_home_IP
```

### Pour afficher les adresses IP actives :
```bash
./1-show_attached_IPs
```

### Pour écouter sur le port 98 :
```bash
sudo ./2-port_listening_on_localhost
```

Dans un autre terminal, vous pouvez vous connecter avec :
```bash
telnet localhost 98
```

## Concepts Clés

1. **Fichier hosts**
   - Fichier système qui fait correspondre des noms d'hôtes à des adresses IP
   - Situé dans `/etc/hosts`
   - Utilisé avant la consultation des serveurs DNS

2. **Adresses IP**
   - IPv4 : Format standard (ex: 192.168.1.1)
   - localhost : 127.0.0.1 (ou 127.0.0.2 après modification)
   - Interface loopback : Interface virtuelle pour la communication locale

3. **Ports**
   - Point d'accès pour les communications réseau
   - Port 98 : Port non standard utilisé dans cet exercice
   - Netcat : Outil polyvalent pour les communications réseau 
