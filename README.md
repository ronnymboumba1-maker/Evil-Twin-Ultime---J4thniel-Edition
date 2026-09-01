# 🎯 EVIL TWIN ULTIME - JATHNIEL EDITION

**Evil Twin Ultime** est un outil avancé de test d'intrusion WiFi avec interface graphique et mode stealth. Il permet de créer un point d'accès malveillant identique à un réseau cible pour capturer les identifiants et intercepter le trafic.

## 🚨 AVERTISSEMENT LÉGAL

```

╔══════════════════════════════════════════════════════════════════════╗
║                                                                      ║
║   ⚠️  USAGE STRICTEMENT ÉDUCATIF ET ACADÉMIQUE                     ║
║                                                                      ║
║   Cet outil est conçu pour des tests de sécurité dans le cadre      ║
║   d'un laboratoire isolé et autorisé.                               ║
║                                                                      ║
║   L'utilisation de cet outil sur des réseaux sans autorisation     ║
║   est ILLÉGALE et peut entraîner des poursuites judiciaires.        ║
║                                                                      ║
║   L'utilisateur est SEUL RESPONSABLE de l'usage de cet outil.      ║
║                                                                      ║
╚══════════════════════════════════════════════════════════════════════╝

```

## 📋 TABLE DES MATIÈRES

1. [Fonctionnalités](#-fonctionnalités)
2. [Architecture](#-architecture)
3. [Installation](#-installation)
4. [Utilisation](#-utilisation)
5. [Configuration](#-configuration)
6. [Dépannage](#-dépannage)
7. [Licence](#-licence)

---

## 🚀 FONCTIONNALITÉS

### 🔷 Couche 1 : Infrastructure Réseau
| Fonctionnalité | Description |
|----------------|-------------|
| **Scan WiFi** | Détection des réseaux environnants |
| **Multi-interface** | Support 2.4GHz et 5GHz |
| **BSSID Spoofing** | Copie de l'adresse MAC cible |
| **Channel Hopping** | Changement automatique de canal |
| **Interface at0** | Gestion automatique de l'interface AP |

### 🔷 Couche 2 : Attaque Active
| Fonctionnalité | Description |
|----------------|-------------|
| **Evil Twin AP** | Point d'accès malveillant identique |
| **Deauth Attack** | Déconnexion des clients légitimes |
| **Beacon Flood** | Inondation de balises |
| **PMKID Capture** | Capture du handshake |
| **Jamming sélectif** | Ciblage des clients spécifiques |

### 🔷 Couche 3 : Interception
| Fonctionnalité | Description |
|----------------|-------------|
| **SSL Strip** | Désactivation du HTTPS |
| **DNS Spoofing** | Redirection DNS conditionnelle |
| **Session Hijack** | Capture et réinjection de cookies |
| **Traffic Analysis** | Classification du trafic |

### 🔷 Couche 4 : Ingénierie Sociale
| Fonctionnalité | Description |
|----------------|-------------|
| **Captive Portal** | Page de phishing personnalisable |
| **Credential Harvesting** | Capture des identifiants |
| **2FA Bypass** | Interception des codes |

### 🔷 Couche 5 : Évasion
| Fonctionnalité | Description |
|----------------|-------------|
| **Stealth Mode** | Opération discrète |
| **WIDS Evasion** | Contournement de détection |
| **Anti-forensics** | Nettoyage automatique des traces |
| **MAC Spoofing** | Changement aléatoire de MAC |

### 🔷 Interface
| Fonctionnalité | Description |
|----------------|-------------|
| **Menu interactif** | CLI complète et intuitive |
| **Statistiques temps réel** | Affichage des métriques |
| **Dashboard** | Vue d'ensemble |
| **Export** | Sauvegarde des données |

---

## 🏗️ ARCHITECTURE

```

┌─────────────────────────────────────────────────────────────────────────────┐
│                          EVIL TWIN ULTIME                                   │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  ┌────────────────────────────────────────────────────────────────────┐    │
│  │                      MENU PRINCIPAL                                │    │
│  │  [1] Scan  [2] Cible  [3] Attaque  [4] Stealth  [5] Stop         │    │
│  │  [6] Victimes  [7] Credentials  [8] Statut  [9] Config  [0] Quit │    │
│  └────────────────────────────────────────────────────────────────────┘    │
│                                    │                                         │
│  ┌────────────────────────────────────────────────────────────────────┐    │
│  │                         CORE ENGINE                                │    │
│  ├────────────────────────────────────────────────────────────────────┤    │
│  │  • Database Manager  • Event Bus  • State Manager  • Thread Pool │    │
│  └────────────────────────────────────────────────────────────────────┘    │
│                                    │                                         │
│  ┌────────────────────────────────────────────────────────────────────┐    │
│  │                       MODULES                                      │    │
│  ├───────────────┬───────────────┬───────────────────────────────────┤    │
│  │  Reconnaissance│   Attaque    │  Interception                     │    │
│  │  ├─ Scanner    │  ├─ Evil Twin│  ├─ SSL Strip                    │    │
│  │  ├─ Mapping    │  ├─ Deauth   │  ├─ DNS Spoof                    │    │
│  │  └─ Cloner     │  └─ Flood    │  └─ Session Hijack               │    │
│  ├───────────────┼───────────────┼───────────────────────────────────┤    │
│  │  Social       │  Post-Exploit │  Évasion                         │    │
│  │  ├─ Phishing   │  ├─ Injection │  ├─ Stealth                     │    │
│  │  ├─ Templates  │  ├─ Pivoting  │  ├─ Anti-forensics               │    │
│  │  └─ Harvest    │  └─ Exfil     │  └─ WIDS Evasion                │    │
│  └───────────────┴───────────────┴───────────────────────────────────┘    │
│                                    │                                         │
│  ┌────────────────────────────────────────────────────────────────────┐    │
│  │                       COUCHES BASES                                │    │
│  ├────────────────────────────────────────────────────────────────────┤    │
│  │  • Scapy  • NetfilterQueue  • Socket  • Subprocess  • SQLite     │    │
│  └────────────────────────────────────────────────────────────────────┘    │
└─────────────────────────────────────────────────────────────────────────────┘

```

---

## 💻 INSTALLATION

### Prérequis Système

```bash
# Ubuntu / Debian / Kali
sudo apt-get update
sudo apt-get install -y \
    aircrack-ng \
    dnsmasq \
    iptables \
    wireless-tools \
    python3-pip \
    python3-venv \
    libnetfilter-queue-dev \
    libnfnetlink-dev
```

Installation Python

```bash
# Cloner le dépôt
git clone https://github.com/JATHNIEL/evil-twin-ultime.git
cd evil-twin-ultime

# Créer un environnement virtuel
python3 -m venv venv
source venv/bin/activate

# Installer les dépendances
pip install -r requirements.txt

# Vérifier l'installation
python3 evil_twin.py --help
```

Vérification des outils

```bash
# Vérifier que les outils sont installés
which airbase-ng     # /usr/sbin/airbase-ng
which aireplay-ng    # /usr/sbin/aireplay-ng
which dnsmasq        # /usr/sbin/dnsmasq
which iptables       # /sbin/iptables
```

---

🎮 UTILISATION

Lancement

```bash
# IMPORTANT: Nécessite les privilèges root
sudo python3 evil_twin.py
```

Menu Principal

```
[1] 🔍 Scanner les réseaux       - Détecte les réseaux WiFi environnants
[2] 🎯 Sélectionner une cible    - Choisir le réseau à cloner
[3] 🚀 Lancer l'attaque (Normal) - Mode standard
[4] 🚀 Lancer l'attaque (Stealth)- Mode discret
[5] 🛑 Arrêter l'attaque         - Arrête et nettoie
[6] 👥 Voir les victimes         - Liste des clients connectés
[7] 🔑 Voir les credentials      - Identifiants capturés
[8] 📊 Statut                    - Vue d'ensemble
[9] ⚙️ Configurer                - Paramètres
[0] ❌ Quitter                   - Quitter le programme
```

Exemple Complet

```bash
# 1. Démarrer
sudo python3 evil_twin.py

# 2. Scanner les réseaux
[1] 🔍 Scanner les réseaux
📊 5 réseaux trouvés:
  1. FreeWifi - 00:11:22:33:44:55 (Canal 6)
  2. Orange - AA:BB:CC:DD:EE:FF (Canal 1)
  
# 3. Sélectionner la cible
[2] 🎯 Sélectionner une cible
Sélectionnez un réseau: 1
✅ Cible sélectionnée: FreeWifi

# 4. Lancer l'attaque
[3] 🚀 Lancer l'attaque (Mode Normal)
🚀 Démarrage de l'attaque Evil Twin
✅ Attaque complète démarrée

# 5. Surveiller
[6] 👥 Voir les victimes
👥 VICTIMES:
  AA:BB:CC:DD:EE:FF - iPhone-15 (iOS)

[7] 🔑 Voir les credentials
🔑 CREDENTIALS:
  admin:password123 (phishing)

# 6. Arrêter
[5] 🛑 Arrêter l'attaque
🛑 Attaque arrêtée

# 7. Quitter
[0] ❌ Quitter
👋 Au revoir!
```

---

⚙️ CONFIGURATION

Paramètres Disponibles

Paramètre Description Valeurs possibles Défaut
Interface Interface WiFi wlan0, wlan1, etc. wlan0
Stealth Mode Mode discret ON/OFF OFF
WIDS Evasion Contournement de détection ON/OFF ON
Channel Canal de l'AP 1-11 (2.4GHz) / 36-165 (5GHz) 6
Gateway IP de la passerelle IP valide 192.168.1.1
Netmask Masque réseau Masque valide 255.255.255.0
DHCP Range Plage DHCP Plage IP 192.168.1.100-200

Modification des Paramètres

```
[9] ⚙️ Configurer

⚙️ CONFIGURATION:
  1. Interface: wlan0
  2. Stealth Mode: OFF
  3. WIDS Evasion: ON

Choisir un paramètre (1-3, 0 pour retour): 1
Nouvelle interface (ex: wlan0): wlan1
✅ Interface changée: wlan1
```

---

🛠️ DÉPANNAGE

Erreurs Courantes

Erreur Solution
Permission denied Exécuter avec sudo
airbase-ng not found sudo apt-get install aircrack-ng
dnsmasq not found sudo apt-get install dnsmasq
Interface at0 not found Vérifier que airbase-ng est lancé
Connection timeout Vérifier le réseau cible
SSL Strip error Vérifier netfilterqueue

Vérification des Dépendances

```bash
# Vérifier les outils système
sudo airbase-ng --help
sudo aireplay-ng --help
sudo dnsmasq --help
sudo iptables --help
sudo iwconfig --help

# Vérifier les modules Python
python3 -c "import scapy; print('OK')"
python3 -c "import netfilterqueue; print('OK')"
python3 -c "import requests; print('OK')"
```

Nettoyage Manuel

```bash
# En cas de blocage
sudo iptables -t nat -F
sudo iptables -F
sudo pkill airbase-ng
sudo pkill dnsmasq
sudo ifconfig at0 down
sudo ifconfig at0 del
```

---

📊 BASE DE DONNÉES

Structure

```sql
-- Victimes
CREATE TABLE victims (
    id INTEGER PRIMARY KEY,
    mac TEXT UNIQUE,
    hostname TEXT,
    ip TEXT,
    os TEXT,
    first_seen TEXT,
    last_seen TEXT
);

-- Credentials
CREATE TABLE credentials (
    id INTEGER PRIMARY KEY,
    victim_id INTEGER,
    username TEXT,
    password TEXT,
    type TEXT,
    timestamp TEXT
);

-- Handshakes
CREATE TABLE handshakes (
    id INTEGER PRIMARY KEY,
    bssid TEXT,
    client_mac TEXT,
    data TEXT,
    timestamp TEXT
);

-- Logs
CREATE TABLE logs (
    id INTEGER PRIMARY KEY,
    level TEXT,
    module TEXT,
    message TEXT,
    timestamp TEXT
);
```

---

📝 NOTES DE VERSION

v1.0 - 2026-09-01

· ✅ Scan WiFi complet
· ✅ Evil Twin AP avec airbase-ng
· ✅ Deauth attack avec aireplay-ng
· ✅ Beacon flood avec scapy
· ✅ Serveur de phishing
· ✅ SSL Strip complet
· ✅ DNS Spoofing
· ✅ Session Hijack
· ✅ Stealth Mode
· ✅ WIDS Evasion
· ✅ Anti-forensics
· ✅ Base de données SQLite
· ✅ Menu interactif

---