# Custom Hidden Function Furniture

**Olin College of Engineering | Spring 2024**

Designed and fabricated a custom stool for a senior citizen with mobility challenges, focusing on human-centered accessibility, height adaptability, lightweight construction, and discreet storage. The project involved iterative CAD design, TIG welding of aluminum, and balancing aesthetic and functional requirements.

---

## The Problem

The client required a stool that could assist with reaching elevated surfaces in the kitchen, while remaining unobtrusive when not in use. Key constraints included:  

- **Human-centered design:** Adapted for senior citizen use  
- **Height adaptability:** Incremental steps of 1 ft and 2 ft  
- **Compact storage:** Collapsible or minimal footprint  
- **Aesthetic integration:** Must blend seamlessly into kitchen design  
- **Lightweight and safe:** Strong enough to support the user, easy to move  

---

## Concept Development

Explored multiple concepts including foldable wooden stools, telescoping aluminum structures, and hybrid collapsible frames. Using SolidWorks CAD modeling, I evaluated:

- Structural strength under user load  
- Folding mechanism and storage footprint  
- Ease of fabrication using TIG welding  

The final design uses a TIG-welded aluminum frame with integrated foot supports, chosen for its combination of lightweight construction, durability, and manufacturability. Iterations focused on harmonizing the stool’s aesthetic integration with functional requirements.

<div style="border:1px solid #ccc; padding:5px;">

  ![CAD model of custom stool](/mirachew-website/images/stool_cad.png)

  <br><em>CAD model showing overall design and frame configuration.</em>
</div>

---

## Material Selection & Rationale

The stool’s materials were chosen to balance **weight, manufacturability, and aesthetics** while meeting the accessibility needs of an older user.

- **Frame material:** Aluminum 6061-T6 square tubing (1×1×⅛ in) was selected over mild steel to reduce overall weight while maintaining sufficient stiffness and strength.  
  - Aluminum: 0.526 lb/ft × 286 in ÷ 12 in/ft ≈ 12.5 lb
  - Steel: 1.44 lb/ft × 286 in ÷ 12 in/ft ≈ 34.3 lb
  - Aluminum reduced the frame weight by approximately **64 %**, significantly improving portability for the user.
- **Surface material:** I chose walnut wood for the stool surface to match the user’s kitchen interior finishes.  
  - The 12″ × 18″ × 1″ and 12″ × 16″ × 1″ walnut panels provided visual warmth and a tactile surface that complemented the aluminum frame’s minimal aesthetic.
- Including weld filler, paint, and the two walnut surfaces, the **total assembly weight** was estimated around **18–20 lb**, still manageable for the user to carry safely and comfortably.


The final stool assembly was slightly heavier than initial projections due to the nested design and finishing materials, but the aluminum construction successfully balanced strength, usability, and aesthetic integration for an accessible final product.


---

## Overview / My Role & Contributions

I led the full design and fabrication process, translating user needs into a functional, manufacturable solution:

- Developed parametric models in SolidWorks 
- Performed finite element analysis (FEA) to validate strength and stiffness before fabrication  
- Fabricated the stool using TIG welding on aluminum tubing  
- Tested weld strength and overall stability through hands-on trials  
- Optimized folding mechanism for minimal footprint while preserving usability  

<div style="border:1px solid #ccc; padding:5px;">

  ![Finished stool before painting](/mirachew-website/images/stool_pre-paint.png)

  <br><em>Fabricated aluminum frame prior to coating and assembly with walnut seat.</em>
</div>

This project strengthened skills in human-centered mechanical design, concept development, and hands-on fabrication, combining aesthetic iteration with FEA-based structural validation to balance analysis, practicality, and usability.

---

## Testing & Validation

### Finite Element Analysis (FEA)

Before fabrication, a finite element analysis (FEA) was conducted in SolidWorks Simulation to validate the stool’s strength, stiffness, and safety margins under realistic loading conditions.

#### FEA Setup
- **Materials:** 6061-T6 aluminum frame, walnut wood seat (included in static simulations)  
- **Load:** 980 N downward to represent a 110 lbs user with a 2× safety factor  
- **Constraints:** Fixed supports at leg bottoms  
- **Simulations:** Static stress/strain and linear buckling  

The static analysis included both the aluminum frame and walnut seat to capture realistic load transfer and deflection.  
The buckling study isolated the aluminum frame to analyze structural instability modes, as the wood top primarily distributed load but contributed minimal stiffness against global buckling.

#### Results
- **Aluminum (6061-T6) Yield Strength:** 275 MPa  
- **Maximum von Mises Stress:** ≈ 10 MPa  
- **Maximum Strain:** ≈ 0.011 mm/mm  
- **Factor of Safety:** 27  
- **Buckling Load Factor:** 307  

These results confirmed the stool could withstand over 300× the expected user load before buckling, validating both the weld and tubing geometry for real-world use.

<div style="border:1px solid #ccc; padding:5px;">

  ![Stool stress distribution](/mirachew-website/images/stool_stress_plot.png)

  <br><em>Static stress (von Mises) distribution with aluminum and walnut assembly under 980 N load.</em>
</div>

<div style="border:1px solid #ccc; padding:5px;">

  ![Stool strain distribution](/mirachew-website/images/stool_strain_plot.png)

  <br><em>Strain distribution highlighting localized deformation near welded joints.</em>
</div>

<div style="border:1px solid #ccc; padding:5px;">

  ![Stool factor of safety plot](/mirachew-website/images/stool_factor_of_safety.png)

  <br><em>Factor of Safety (FOS) plot for the full stool assembly; minimum value ≈ 27.</em>
</div>

<div style="border:1px solid #ccc; padding:5px;">

  ![Stool buckling mode](/mirachew-website/images/stool_buckling_plot.png)

  <br><em>First buckling mode shape (load factor = 307) for aluminum frame only.</em>
</div>

#### Interpretation
The FEA confirmed that the welded aluminum structure comfortably exceeded required safety margins, demonstrating stiffness and durability under a 980 N applied load.  
This analysis guided final weld sizing and tubing selection before fabrication, ensuring structural performance while minimizing weight.

**Result:** The stool reliably supported the user’s weight, folded compactly, and visually integrated into the home environment.

### Physical Testing
- Bench-tested weld joints by applying bending force to failure  
- Verified stool stability at each height increment (1 ft / 2 ft)  
- Confirmed ease of collapse and storage without compromising safety  

<div style="border:1px solid #ccc; padding:5px;">

  ![Custom stool collapsed](/mirachew-website/images/stool_compact.png)

  <br><em>Stool collapsed for compact storage.</em>
</div>

<div style="border:1px solid #ccc; padding:5px;">

  ![Custom stool fully extended](/mirachew-website/images/stool_expanded.png)

  <br><em>Stool fully extended at maximum height.</em>
</div>

---

## Technical Tools & Skills

**SolidWorks (Parametric CAD & Simulation)** | **FEA & Structural Validation** | **TIG Welding (Aluminum)** | **Human-Centered Mechanical Design** | **Load & Bending Analysis** | **Prototype Testing & Iteration**  

---

## Key Challenges & Learnings

- Designing a compact, foldable frame that maintains strength for senior use  
- Translating CAD models into precise, weldable aluminum components  
- Validating design safety through both FEA and real-world testing  
- Balancing weight, rigidity, and aesthetic goals for a safe and practical design  

This project underscored the importance of combining engineering analysis with hands-on fabrication, ensuring that human-centered design is supported by measurable structural validation.
