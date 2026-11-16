# Hi, ich bin Dennis 👋

**Automation & Robotics Engineer – Systemintegration · Humanoide Robotik · Simulation & Logistikautomation**

Ich komme aus der praktischen Logistik- und Materialflussautomatisierung und arbeite an der Schnittstelle zwischen IT-Systemen, Simulation und echter Roboter-Hardware. Mein Fokus liegt darauf, bestehende Frameworks (ROS 2, NVIDIA Isaac Sim / Isaac Lab, Pinocchio, Unity) pragmatisch zu verbinden, Pipelines aufzubauen und Bewegungsabläufe sicher vom digitalen Zwilling auf reale Systeme zu bringen.

---

## 🪪 Auf einen Blick

| | |
|---|---|
| **Hintergrund** | Logistikautomation (MFR/MFC, Prozessdaten/SQL) & angewandte Robotik-Integration |
| **Plattform-Praxis** | Humanoider Roboter (2 × 7-DOF-Arme, Dexterous Hands, Stereo-/RGB-D-Kameras) |
| **Schwerpunkte** | VR-Teleoperation · Pick-and-Place-Pipelines · Isaac Sim / Isaac Lab · ROS 2 (Python) |
| **Arbeitsweise** | Pragmatisches Rapid Prototyping (inkl. AI-assisted Development), erst in der Simulation und offline testen, dann schrittweise auf der Hardware validieren |
| **Sprachen** | Deutsch · Polnisch · Englisch |

---

## 🗺️ Themen & Projekte, an denen ich arbeite

### 🥽 Teleoperation & Steuerung
- **VR-Teleoperation (Meta Quest 3, Unity → ROS 2):** Ansteuerung beider Roboterarme über VR-Controller inklusive Kamera-Stream zurück ins Headset.
- **Retargeting & Mapping:** Anpassung und Kalibrierung der Koordinatensysteme zwischen VR-Setup und Roboter, damit linker und rechter Arm symmetrisch und sauber reagieren.
- **Hand-Ansteuerung:** Einbindung von Greif- und Schließsequenzen für mehrgliedrige Roboterhände (Dexterous Hands) per Trigger und Hand-Tracking.
- **Operator-Tools:** Web-Oberflächen und einfache Skripte zum Starten, Überwachen und Steuern von Abläufen.

### 🦾 Bewegungsplanung & Kinematik-Integration
- **Dual-Arm-IK in Python (Pinocchio):** Einsatz und Anpassung eines Pinocchio-basierten IK-Solvers als schlanke Alternative zu MoveIt 2 für flüssiges Streaming.
- **Praktisches Limit- & Singularitäts-Handling:** Begrenzung von Schrittweiten und Arbeitsraum-Radien, damit die Arme im Betrieb nicht in gestreckte Singularitäten oder Gelenklimits laufen.
- **Sichere Ausführung auf der Hardware:** Offline-Vorabprüfung von Pfaden, schrittweise Verifikation der Gelenkpositionen und klare Trennung zwischen Software-Freigabe und physischem Not-Halt.

### 📦 Pick-and-Place & Logistik-Use-Cases
- **Regal-Picking auf realer Hardware:** Durchgängiger Ablauf von der Zielvorgabe über kollisionsgeprüfte Waypoints bis zum Greifen und Ablegen – Schritt für Schritt von ~147 s auf ~56 s Zykluszeit optimiert.
- **Kisten- & Förderband-Szenarien (Sim):** Aufbau virtueller Versandanlagen- und Bin-Picking-Szenarien zur Erprobung von Greif- und Hebevorgängen.

### 🌐 Simulation, Digital Twin & Reinforcement Learning
- **NVIDIA Isaac Sim & Isaac Lab:** Aufbau digitaler Zwillinge (USD/URDF) von Arbeitszellen, Förderbändern und Robotermodellen.
- **RL-Training (PPO / `rsl_rl`):** Training, Parameter-Tuning und Auswertung von Policies in der Simulation für Balance, Gehen mit Traglast und Greifbewegungen.
- **Sim-to-Real-Abgleich:** Gemeinsame Python-/ROS-2-Pipeline für Simulation und echten Roboter sowie Messung realer Gelenk-Verzögerungen (Latenzen), um das Simulationsmodell realistischer einzustellen.

### 👁️ Kameras & Objekterkennung
- **Vision-Integration:** Einbindung von YOLO / YOLO-World und SAM 2 in Docker-Containern zur Erkennung von Kisten und Produkten im Kamerabild.
- **Praxiserkenntnis:** Da rein bildbasierte End-to-End-Policies bei wechselndem Licht schnell instabil wurden, setze ich bei realen Greifabläufen lieber auf nachvollziehbare, explizit überprüfbare Zwischenschritte.

---

## 🚀 Ausgewählte Repositories & Prototypen

| Projekt | Kurzbeschreibung |
|---|---|
| **VR Teleop Pro** | Quest 3 → Unity → ROS 2 → Python-IK-Ansteuerung auf der realen Hardware |
| **Teleop Twin** | Umschaltbare Steuerungspipeline zum Testen in Isaac Sim oder am echten System |
| **Bin-Picking Twin** | Virtuelle Arbeits- und Versandzelle in Isaac Lab für RL-Experimente (Balance, Gehen, Greifen) |
| **Order Terminal** | Kiosk- und Steuerungs-Interface zur Auslösung validierter Pick-Abläufe |

---

## 🛠️ Tech-Stack

`Python` `ROS 2 (Humble / rclpy)` `NVIDIA Isaac Sim` `NVIDIA Isaac Lab` `Pinocchio`
`Unity (C# / Quest 3)` `Docker` `Linux` `Git` `SQL (MS SQL / IBM Db2)` `Bash / PowerShell`
`PyTorch` `NumPy` `YOLO` `URDF / USD` `MoveIt 2 (Basics)`

---

## 📫 Kontakt

- GitHub: [polskiesmaki](https://github.com/polskiesmaki)
- E-Mail: dennis.glowacki@gmx.de

> *Hinweis: Alle Beschreibungen sind allgemein gehalten und enthalten keine vertraulichen Unternehmens- oder Projektdaten.*
