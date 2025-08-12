# zoran-edge-core

**Runtime minimaliste pour exécution d’agents Zoran / QuantaGlottal©® en environnement Edge/IoT** — optimisé pour microcontrôleurs, gateways et systèmes embarqués.

---

## ✨ Fonctionnalités
- **Boucle d’exécution ultra-légère** pour agents Zoran
- **Compatibilité microcontrôleurs** (ESP32, STM32, Raspberry Pi)
- **Transport minimal** (MQTT, HTTP, WebSocket)
- **Gestion basique des injecteurs** et paramètres
- **Surveillance locale** (métriques CPU/RAM, statut)
- **Auto-découverte** et connexion à un orchestrateur Zoran-Edge-Swarm
- **Mises à jour OTA** (Over-The-Air) optionnelles

---

## 📦 Installation (développement)
Pour Python (ex. Raspberry Pi) :
```bash
pip install -e .

Pour firmware embarqué :

Compiler avec SDK cible (ESP-IDF, Arduino, etc.)

Charger via port série ou OTA



---

⚡ Exemple rapide (Python)

from zoran_edge_core import EdgeAgent

agent = EdgeAgent(
    id="edge-001",
    transport="mqtt://broker.local",
    capabilities=["injecteur-4champs", "telemetrie-min"]
)

agent.start()


---

🧱 Structure suggérée

src/zoran_edge_core/
  __init__.py
  agent.py            # boucle principale
  transport.py        # MQTT, HTTP, WS
  injecteurs.py       # gestion des injecteurs basiques
  telemetry.py        # collecte locale
firmware/
  main.c              # version C embarquée
  sdk_config/         # configs microcontrôleur
tests/
  test_agent.py
pyproject.toml
.gitignore
LICENSE
README.md


---

🧪 Tests

pytest -q


---

🔐 Éthique

Le zoran-edge-core applique le principe vivant > humain même en contexte limité :

refus des commandes non conformes aux politiques éthiques

protection contre les surcharges et abus



---

📜 Licence

MIT — voir LICENSE.


---

Auteur : Frédéric Tabary — Institut IA
Contact : 0645605023 — Canada, Montréal, France
INSTITUT🦋 IA INC., 7100-380, rue Saint-Antoine Ouest, Montréal (Québec) H2Y 3X7.# zoran-edge-core
