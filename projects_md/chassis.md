# Baja SAE Chassis Design & Fabrication

**Olin College of Engineering | Spring 2023 - Fall 2024**

As part of Olin College's Baja SAE team, I led the chassis design, analysis, and fabrication of an off-road endurance vehicle built for national competition. The project centered on balancing driver ergonomics, service accessibility, and safety performance within SAE rules.

I was responsible for designing the full roll cage and cockpit geometry, running FEA-based impact and rollover analyses, and welding/assembly of the final frame. The work emphasized structural integrity under crash loading, manufacturability with chromoly tubing, and rapid iteration between CAD, FEA, and on-track testing.

---

## Design Process

The chassis was modeled in SolidWorks using 3D sketches and weldments, carefully ordered to define main members first and trim dependent pieces for accurate joint intersections. I focused on cockpit comfort to ensure the average driver fit comfortably while maintaining engine access and serviceability for rapid drivetrain installation. I constantly referenced the thick Baja SAE rulebook to ensure that each design decision was legal.

<div style="text-align: center; margin: 20px 0;">

<div style="display: inline-block; text-align: center; border: 1px solid #ccc; padding: 10px; background-color: #fafafa; width: 900px;">

![Baja Chassis Design - FEA Setup](/mirachew-website/images/static_1.PNG)

<br><em>Initial chassis FEA study showing stress distribution and member loading.</em>

</div>

</div>

---

## Finite Element Analysis

I conducted static load and impact simulations to evaluate crash performance and rollover resistance.

This analysis guided reinforcement of key regions, particularly near the front suspension mounts and cockpit supports, while retaining rule compliance throughout. I also added gussets where stress-concentrations could not be reduced via base structure redesign.

Through iterative redesign, I increased the minimum factor of safety from 2.8 to 4.8, meeting and exceeding the targeted threshold for driver protection of FOS 3.

<div style="text-align: center; margin: 20px 0;">

<div style="display: inline-block; text-align: center; border: 1px solid #ccc; padding: 10px; background-color: #fafafa; width: 900px;">

![Baja Chassis Design - FEA Results](/mirachew-website/images/static_3.PNG)

<br><em>Improved chassis iteration showing increased minimum factor of safety.</em>

</div>

</div>

---

## Fabrication & Testing

<div style="display: flex; gap: 20px; align-items: start; margin: 20px 0;">

<div style="flex: 1;">

I fabricated the chassis via MIG-welding SAE-quality chromoly 4130 steel. I utilized plywood fixtures to hold tubes in place while welding. I led the welding process, ensuring alignment and minimizing distortion across joints. At competition, the car passed technical inspection and completed the full endurance race! The frame remained fully intact throughout, validating the design — while real-world failures occurred in suspension control arms and drivetrain guarding, not the chassis itself.

</div>

<div style="flex-shrink: 0; align-self: flex-start;">

<div style="display: inline-block; text-align: center; border: 1px solid #ccc; padding: 10px; background-color: #fafafa; width: 450px;">

![Priming and Painting Chassis](/mirachew-website/images/chassis_midpaint.png)

<br><em>Fully welded chassis during priming and painting.</em>

</div>

</div>

</div>

---

## My Role & Contributions

- **Lead Design:** Developed full chassis model for SAE rule compliance.
- **FEA Analysis:** Performed static and impact analyses to crash scenarios
- **Fabrication Lead:** Oversaw MIG welding, tubing prep, and alignment jigs.
- **Integration Lead:** Coordinated integration of drivetrain, suspension, and safety subsystems.

---

## Key Results

- Increased minimum FOS from 2.8 to 4.8 through iterative simulation and redesign.
- Successfully passed inspection and completed endurance event without frame failures.
- Improved assembly serviceability and cockpit ergonomics for multi-driver operation.

<div style="display: flex; gap: 15px; justify-content: center; margin: 20px auto; flex-wrap: wrap; align-items: flex-start;">

<div style="text-align: center; border: 1px solid #ccc; padding: 10px; background-color: #fafafa; height: 350px; display: flex; flex-direction: column; justify-content: space-between;">

<img src="/mirachew-website/images/baja_front_pic.png" alt="Welding at Competition" style="height: calc(350px - 60px); width: auto; object-fit: contain;">

<br><em>Welding repairs and adjustments at competition.</em>

</div>

<div style="text-align: center; border: 1px solid #ccc; padding: 10px; background-color: #fafafa; height: 350px; display: flex; flex-direction: column; justify-content: space-between;">

<img src="/mirachew-website/images/baja_1.png" alt="Compete" style="height: calc(350px - 60px); width: auto; object-fit: contain;">

<br><em>Fully functioning car driving back to pit.</em>

</div>

</div>

---

## Key Challenges & Learnings

During the design process, I learned that accurately modeling joint geometry in FEA is critical for reliable stress analysis. While my initial simulations successfully guided structural improvements and achieved the target factor of safety, I later received feedback that adding fillets to all joint intersections would have improved both the accuracy of the results and the visualization of how stress concentrations distribute and flow through the structure.

This insight highlighted the importance of modeling geometry as close to physical reality as possible—particularly for welded joints where material naturally transitions smoothly rather than meeting at sharp angles. In future FEA work, I'll prioritize incorporating filleted joints to capture more realistic stress distributions and ensure the analysis better reflects actual component behavior under load.

- Balancing structural optimization with SAE rule compliance across multiple design iterations
- Coordinating fabrication timelines with testing and competition preparation
- Learning to incorporate constructive feedback into technical methodology and improve analysis fidelity

---

## Technical Tools & Skills

- **SolidWorks** (3D Sketch, Weldments, FEA)
- **MIG Welding**
- **Rulebook Compliance**
- **Vehicle Integration**
- **Shop Safety**
- **Leadership**
