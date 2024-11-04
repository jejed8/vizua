![synoptique](https://github.com/user-attachments/assets/af4ebf1a-1a1b-47bf-a080-86081850dafc)# Vizua

## Concept 
L'expérience est une installation immersive où l'utilisateur joue sur un clavier MIDI et voit des visuels dynamiques se déployer autour de lui en réalité virtuelle. Chaque note déclenche des animations spectaculaires qui réagissent en temps réel, créant un spectacle audiovisuel captivant et interactif.

<img width="1710" alt="Screenshot 2024-11-04 at 3 59 05 PM" src="https://github.com/user-attachments/assets/0d1631bd-a0b8-48c1-8a90-9e10aeeb605e">

## Devis

### Location / emprunt 
- Caque VR (oculus)
- Ordinateur (Étant capable de supporter les requis logiciel)
- Haut-Parleur Surround x4
- Console de son

### Materiel fourni par l'artiste 
- Clavier MIDI Launchkey 49 Ableton


## Synoptique
![synoptique 2](https://github.com/user-attachments/assets/2f1cc33c-ffad-4410-a990-d80f3570d89c)

### Entrée

- **Clavier MIDI** : Envoie des signaux MIDI au DAW.
- **DAW (Digital Audio Workstation)** :
  - Reçoit le signal MIDI.
  - Modifie les sons (EQ, effets, etc.).
  - Envoie les données audio/MIDI à PyTorch et à TouchDesigner.

### Analyse AI

- **Framework PyTorch** :
  - Reçoit le signal audio/MIDI modifié du DAW.
  - Analyse le son (détection de motifs, classification d'émotions).
  - Envoie les résultats d'analyse à TouchDesigner via OSC/WebSocket.

### Communication

- **OSC / WebSocket** :
  - Transporte les données d'analyse de PyTorch vers TouchDesigner en temps réel.
  - Synchronise les échanges de données entre le DAW, PyTorch et TouchDesigner.

### Création Visuelle

- **TouchDesigner** :
  - Reçoit les données MIDI/audio et les résultats d'analyse de PyTorch.
  - Crée des visuels dynamiques basés sur les notes jouées et l'analyse AI.
  - Intègre des éléments 3D et de l'instancing pour des visuels complexes.

### Rendu VR

- **OpenVR CHOP/TOP** :
  - Configure l'environnement de rendu stéréoscopique.
  - Relie les mouvements du casque VR et des contrôleurs à la caméra virtuelle et aux interactions visuelles.
- **Scène 3D** :
  - Adapte l'espace visuel pour l'immersion totale.
  - Synchronise les éléments visuels avec les mouvements et les interactions de l'utilisateur.

### Interactions et Retours

- **Contrôleurs VR** :
  - Permettent à l'utilisateur de manipuler et interagir avec les visuels.
  - Envoient des signaux à TouchDesigner pour déclencher des animations ou modifier les éléments visuels.
- **Feedback visuel et haptique** :
  - Affiche des réponses visuelles et, si possible, des retours haptiques via les contrôleurs.

### Résumé du Flux

**Clavier MIDI ➔ DAW ➔ Analyse par PyTorch ➔ Transmission OSC/WebSocket ➔ TouchDesigner ➔ Rendu VR (OpenVR).**

**Interaction utilisateur (contrôleurs) ➔ TouchDesigner ➔ Feedback en temps réel.**





