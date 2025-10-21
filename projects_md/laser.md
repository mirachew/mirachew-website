# Laser Wizard Tag

**Olin College of Engineering | Spring 2024**

Laser Wizard Tag is a custom-built, multiplayer game that reimagines traditional laser tag through embedded systems, real-time communication, and interactive hardware design. Players wear custom vests embedded with infrared sensors and LEDs and use a wand to cast “spells.” I led the integration of electrical, mechanical, and software systems — including full circuit design, soldering, programming, and debugging — to bring the system from concept to a fully working, networked prototype.


<div style="text-align:center; border:1px solid #ccc; padding:5px; margin:15px 0;">
<img src="/mirachew-website/images/laser_tag_front_pic.jpg" alt="Laser Wizard Tag Final Prototype" width="45%" style="display:block; margin:auto;">
<br><em>Final laser wizard tag vest.</em>
</div>



---

## Overview

The goal was to create an interactive and immersive game experience that combined embedded electronics, wireless communication, and human-centered mechanical design.  

When a player casts a spell, their wand emits a 940 nm infrared beam detected by sensors on opponents’ vests. The hit triggers haptic feedback and LEDs on the target’s vest, while a central dashboard updates each player’s health in real time. Once a player loses three lives, their vest powers off — signaling that they are “out.”

The project was completed by a four-person team, with my work focusing primarily on electrical design, software development, system integration, and technical leadership.

<a href="https://vigilant-enigma-mz6yg85.pages.github.io/" target="_blank" rel="noopener noreferrer">
Visit the full project website →
</a>


---

## My Role and Responsibilities

I contributed across multiple disciplines, acting as the primary systems integrator and developer.  

**Electrical Design**
- Designed the vest and wand circuits using IR emitters, sensors, vibration motors, and LEDs.  
- Implemented current-balancing and resistor networks to maintain consistent brightness and detection reliability.  
- Selected and tested resistor values (1 Ω for IR LEDs, 2 MΩ for sensors) to optimize range, response time, and heat performance.
- Created a wiring architecture that safely routed power and signal through multiple vest layers using flexible foam and braided sleeving.

**Soldering and Fabrication**
- Personally soldered and assembled hundreds of joints, connecting LEDs, IR sensors, and vibration motors across 4 vests and wands.  
- Debugged shorts, open connections, and voltage inconsistencies.  
- Ensured all wiring was concealed and mechanically protected between vest layers.

**Software Development**
- Programmed the full system using Arduino (C++) with modular object-oriented code: `Player`, `Vest`, and `Wand` classes.  
- Integrated Adafruit IO for real-time updates to a live website dashboard.  
- Developed logic for:
  - Hit detection and LED/haptic feedback timing  
  - Game states and player elimination  
  - Synchronization between multiple ESP8266 boards over Wi-Fi  

**Leadership and Integration**
- Served as the technical lead, coordinating design decisions and system integration.  
- Managed task timelines, ensured compatibility between hardware and code, and provided feedback on teammates’ designs.  
- Troubleshot failures in both hardware and code to achieve reliable, synchronized operation across the full system.

---

## Electrical System Architecture

Each vest featured five sensor panels (four front, one back), each with multiple IR receivers and LED groups. In total, each vest contained 33 IR sensors and 24 LEDs, wired in mixed series-parallel configurations for consistent current draw and redundancy.

- **IR Sensors**: 33 sensors, each paired with a 2 MΩ resistor to limit noise and false triggering  
- **LED Groups**: Four front panels (4 LEDs each) + back panel (8 LEDs)  
- **IR Emitter**: 940 nm diode in the wand, pulsed for short, high-power bursts  
- **Vibration Feedback**: Wand and vest each included a micro vibration motor  
- **Power Source**: 3.7 V 650 mAh LiPo battery regulated through 3.3 V output pin of ESP8266  


<div style="text-align:center; border:1px solid #ccc; padding:5px; margin:15px 0;">
<img src="/mirachew-website/images/laser-tag/circuit_diagram.png" alt="Electrical System Diagram" width="70%" style="display:block; margin:auto;">
<br><em>Basic circuit diagram of each vest.</em>
</div>

<div style="text-align:center; border:1px solid #ccc; padding:5px; margin:15px 0;">
<img src="/mirachew-website/images/laser-tag/esp8266.png" alt="MicroController" width="60%" style="display:block; margin:auto;">
<br><em>ESP8266 controller in housing with circuitry attached.</em>
</div>


A key learning moment came when our first prototype — which powered 24 LEDs in parallel — resulted in **extremely dim lights**. Through testing, I discovered the ESP8266’s current limitation which I mitigated using different resistors. Unfortunately I could not increase the current supplied so the vests are not as bright as intended.

---

## Software Logic and Communication

Each microcontroller handled all game logic for its player, with communication over Wi-Fi for live status tracking.

**Core Features:**
- **IR Hit Detection:** Analog readout from sensor array triggers LED and vibration feedback.  
- **Game Loop:** The main `.ino` script continuously updates each player’s vest and wand states.  
- **Health Tracking:** The `Player` class manages health counters and broadcasts changes to the shared dashboard.  
- **Wi-Fi Integration:** Each ESP8266 connects to an Adafruit IO dashboard using unique credentials for player health visualization.  
- **Fail-Safes:** Automatic vest shutdown once health = 0, preventing further sensor activity.

```cpp
if (playerHealth > 0 && detectHit()) {
  playerHealth--;
  blinkVestLEDs();
  vibrate();
  sendHealthUpdate(playerHealth);
}
```

<div style="text-align:center; border:1px solid #ccc; padding:5px; margin:15px 0;">
<img src="/mirachew-website/images/laser-tag/game_logic.png" alt="Game Logic Code Screenshot" width="70%" style="display:block; margin:auto;">
<br><em>Basic method called each loop to update a player's status and run their player functions.</em>
</div>


<a href="https://github.com/olincollege/wizard-tag/tree/main/wizard-tag-game" target="_blank" rel="noopener noreferrer">
See the github repository here! →
</a>

---

## Mechanical and Material Design

The vests were constructed with comfort, durability, and concealment in mind. Each vest consisted of four layers:

1. Textured pleather (outer shell)
2. Flexfoam (impact absorption and cable routing)
3. Flexfoam (inner protection)
4. Charmeuse lining (comfort against skin)

All wiring was sandwiched between foam layers and routed to a custom 3D-printed ESP8266 enclosure with a latching cover sewn into the left chest.


<div style="text-align:center; border:1px solid #ccc; padding:5px; margin:15px 0;">
<img src="/mirachew-website/images/laser-tag/vest_inside.png" alt="Vest Internal Circuitry" width="60%" style="display:block; margin:auto;">
<br><em>Inside of vest prior to closure with charmeuse lining.</em>
</div>

<div style="text-align:center; border:1px solid #ccc; padding:5px; margin:15px 0;">
<img src="/mirachew-website/images/laser-tag/vest_outside.png" alt="Vest Outside" width="70%" style="display:block; margin:auto;">
<br><em>Finished vest outside view.</em>
</div>




---

## Technical Tools & Skills

**ESP8266 Microcontrollers** | **Circuit Design & Soldering** | **C++ / Arduino Programming** | **SolidWorks (Mechanical CAD)** | **Electrical Prototyping & Debugging** | **System Integration & Testing** | **Team Project Leadership**


---

## Technical Challenges and Learning

This project tested every aspect of my prototyping and debugging skills.

- Electrical: Learned how parallel circuits divide current, and how to design around microcontroller voltage limits.
- Software: Built a modular C++ system integrating multiple hardware components through Wi-Fi.
- Integration: Learned how to debug across systems (mechanical + electrical + software) under tight deadlines.
- Leadership: Balanced team coordination, communication, and technical execution to deliver a robust demo.

Ultimately, the project taught me how to merge mechanical design with embedded systems, prototype quickly, and debug under real-world constraints.

---

## Key Takeaways

- Strengthened practical skills in electronics design, soldering, and debugging
- Built experience programming microcontrollers and real-time systems
- Gained hands-on experience with wireless communication
- Practiced team leadership and interdisciplinary coordination
- Learned to adapt designs rapidly through iterative testing and failure recovery