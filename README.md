# Hi, ich bin Dennis 👋

**Robotics Engineer – Teleoperation · Humanoide Roboter · Simulation & Digital Twins**

Ich entwickle Software, die Menschen und Roboter verbindet: von der VR-Teleoperation eines
zweiarmigen Humanoiden über Inverse Kinematik und Perception bis zum digitalen Zwilling
in Isaac Sim. Am liebsten arbeite ich direkt an der Grenze zwischen Simulation und echter
Hardware.

---

## 🪪 Auf einen Blick

| | |
|---|---|
| **Rolle** | Robotics Engineer (Software, Integration, Teleoperation) |
| **Plattform-Erfahrung** | Humanoider Industrieroboter: 2 × 7-DOF-Arme, Dexterous Hands, Kopf-Stereo, RGB-D, Kraft-Momenten-Sensoren am Handgelenk |
| **Schwerpunkte** | VR-Teleoperation · Dual-Arm-IK · Bin- & Regal-Picking · Isaac Sim / USD · ROS 2 |
| **Arbeitsweise** | Erst offline messen, dann am echten Roboter testen. Sicherheit, Nachvollziehbarkeit, dokumentierte Evidenz |
| **Sprachen** | Deutsch · Polnisch · Englisch |

---

## 🗺️ Robotik-Themen, an denen ich gearbeitet habe

### 🥽 Teleoperation & Mensch-Roboter-Schnittstellen
- **VR-Teleoperation (Meta Quest 3, Unity → ROS 2):** Beide Arme werden in Echtzeit über die Controller gesteuert, das Stereo-Kamerabild des Roboters läuft zurück ins Headset.
- **Motion-Capture-Teleoperation:** Retargeting menschlicher Bewegungen auf Roboter-Gelenkziele.
- **Retargeting-Engineering:** Spiegelsymmetrie zwischen linkem und rechtem Arm, Korrektur des Controller-Koordinatensystems, Kalibrier-Gesten, Analyse von Asymmetrien in aufgezeichneten Daten.
- **Hand- und Greif-Teleoperation:** Finger- und Daumensteuerung einer Dexterous Hand.
- **Kopfsteuerung:** Der Kopf folgt dem Headset, oder die Kamera wird bei Aufnahmen fixiert.
- **Bedienoberflächen:** Web-UIs für Operator, Aufnahme und Training, Sprachausgabe als Statushinweis (Voice Cues/TTS).

### 🦾 Kinematik, IK & Bewegung
- **Streaming-IK für zwei redundante 7-DOF-Arme (Pinocchio):** Damped Least Squares, Nullraum-Steuerung, Warm-Start.
- **Umgang mit Singularitäten:** Begrenzung der Reichweite, Mindestbeugung des Ellbogens als Active-Set-Constraint, Wahl der Neutralhaltung abseits der Gimbal-Lock-Stellung des Handgelenks.
- **Trajektorien & sichere Ausführung:** Quintische Profile, Abstand zu Gelenkgrenzen, Kollisionsprüfung vor der Ausführung, Offline-Planung mit Dry-Run.
- **Gravitationskompensation / Lead-Through:** Nutzlast-Identifikation über die Kraft-Momenten-Sensoren am Handgelenk.

### 👁️ Perception & Sensorik
- **Objekterkennung:** YOLOv8 und Open-Vocabulary-Detektion (YOLO-World), Produkt-Wiedererkennung über Embeddings.
- **3D aus Stereo und RGB-D:** Greifpunkte im Roboter-Basisframe.
- **Kamera-Extrinsik über die kinematische Kette:** Der Kamerapose-Pfad wird mit den gemessenen Gelenkwinkeln berechnet, mit Selbsttest gegen das Robotermodell.
- **AprilTag-Lokalisierung:** Position des Roboters relativ zur Arbeitszelle.
- **Abgleich von URDF, USD und realer Hardware:** Gelenk-Origins, Montage-Transformationen, Massen.

### 📦 Greifen, Bin- & Regal-Picking
- **Regal-Picking-Pipeline:** Erkennung → Greifziel → IK-Plan → Ausführung → Verifikation.
- **Erklärbare Greifmodelle aus Demonstrationen:** Explizites geometrisches Modell statt Black-Box-Policy.
- **Bin-Picking-Zelle als digitaler Zwilling:** Kiste und Produkte in USD, Analyse der Erreichbarkeit vor jedem RL- oder IL-Schritt.
- **Ansteuerung einer Dexterous Hand:** Greif- und Öffnungssequenzen, Diagnose der Mechanik.

### 🌐 Simulation & Digital Twins
- **Isaac Sim 5.x / Isaac Lab:** Szenenaufbau in USD, Artikulationen, Antriebe (Drives), Kollisionsgeometrie, Masseneigenschaften.
- **Sim ↔ Real mit einer Codebasis:** Dieselbe Teleop- und IK-Pipeline steuert die Simulation oder den echten Roboter.
- **Modellpflege:** Konsistenz zwischen URDF, Xacro, USD und MJCF, Vergleich von Hersteller-Modellen per Vorwärtskinematik.

### 🧠 Robot Learning
- **Demo-Recording-Pipeline:** Bilder, Gelenkzustände, Gelenkmomente, Kraft-Momenten-Daten und kommandierte Aktionen werden synchron aufgezeichnet.
- **Datensatz-Qualitätschecks und Export ins LeRobot-Format** (Behavior Cloning / ACT).
- **Ehrliches Learning:** Eine bildbasierte Policy wurde instabil, sobald sich Licht und Hintergrund änderten. Die Konsequenz war eine Architektur mit messbarer, austauschbarer Vision-Komponente.

### 🔧 Systemintegration & Betrieb
- **ROS 2 auf mehreren Rechnern:** DDS/QoS, Docker-Container, Brücken zwischen den Rechnern.
- **Diagnose an echter Hardware:** EtherCAT-/Servo-Fehler, Energie und Laden, Sensor-Bias.
- **Sicherheitskonzept:** Klare Trennung zwischen Planung durch Software und Ausführung durch den Operator.

---

## 🚀 Ausgewählte Projekte (nicht-proprietäre Darstellung)

| Projekt | Inhalt |
|---|---|
| **VR Teleop Pro** | Quest 3 → Unity → ROS 2 → Dual-Arm-Streaming-IK → Roboter; Stereo-Video zurück ins Headset |
| **Teleop Twin** | Eine Pipeline, zwei Ziele: Isaac Sim oder echter Roboter, umschaltbar per Kommando |
| **Bin-Picking Twin** | Arbeitszelle mit Kiste als USD-Digital-Twin, Erreichbarkeitsanalyse, Grundlage für RL/IL |
| **Shelf Picking** | Perception-gestütztes Greifen aus dem Regal mit erklärbarem Greifmodell |
| **Training Studio** | Web-Oberfläche für Aufnahme, Prüfung und Verwaltung von Demonstrationen |

---

## 💡 Was ich aus der Praxis mitnehme

- **Singularitäten verhindern statt auflösen:** Ein gestreckter 7-DOF-Arm kommt allein nicht mehr zurück.
- **Erst die Eingangsdaten prüfen, dann den Solver tunen:** Asymmetrien steckten fast immer in den Zielen, nicht in der IK.
- **„Sollte funktionieren“ ist kein Ergebnis:** Offline reproduzieren, Messwerte mit Datum festhalten.
- **Erklärbare Modelle schlagen Black Boxes,** wenn Licht und Umgebung nicht kontrollierbar sind.

---

## 🛠️ Stack

`Python` `C++` `C#` `ROS 2` `Linux` `Docker` `Git`
`Isaac Sim` `Isaac Lab` `USD` `Unity` `Pinocchio` `MoveIt 2` `MuJoCo`
`OpenCV` `YOLOv8` `PyTorch` `LeRobot` `NumPy` `SciPy`
`Meta Quest 3 / XR` `Motion Capture` `Embedded / MCU`

---

## 🎯 Interessen

Teleoperation & Shared Autonomy · Humanoide Roboter & Locomotion · Digital Twins ·
Perception & Sensorfusion · Mensch-Roboter-Interaktion · Robot Learning · robuste Robotik-Architekturen

---

## 📫 Kontakt

- GitHub: [polskiesmaki](https://github.com/polskiesmaki)
- E-Mail: dennis.glowacki@gmx.de

> Alle Inhalte sind bewusst allgemein gehalten. Es werden keine vertraulichen Produkt-, Kunden- oder Firmendaten veröffentlicht.
