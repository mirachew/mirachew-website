# CNC Mill Treasure Box

**Olin College | September 2025**

Designed and manufactured a custom aluminum box from two 3"×3"×1.5" stock pieces using CNC milling on a Tormach 770M. The project focused on learning CAM setup, GD&T application, and precision alignment using press-fit dowel pins. I modeled the box in Fusion 360, programmed the toolpaths, and performed tolerance checks to achieve a smooth rotating assembly with tight fits.

---

## Objectives

- Develop hands-on experience with CNC milling operations and CAM programming
- Manufacture an assembled two-part aluminum box with rotational motion
- Practice GD&T and press-fit design principles
- Explore manufacturability and tolerance stack-up

---

## Design Overview

The treasure box serves as a small mechanical display piece. The rotating top reveals different images in four circular cutouts on the bottom plate, spinning smoothly about a 0.25" press-fit dowel pin (FN2 fit). Both parts feature shallow pockets and chamfers for aesthetic and functional alignment.

<div style="display: flex; gap: 15px; justify-content: center; margin: 20px auto; flex-wrap: wrap;">

<div style="display: inline-block; text-align: center; border: 1px solid #ccc; padding: 10px; background-color: #fafafa; max-width: 400px;">

![Treasure Box Product](/mirachew-website/images/finished-view.png)

<br><em>Finished treasure box product.</em>

</div>

<div style="display: inline-block; text-align: center; border: 1px solid #ccc; padding: 10px; background-color: #fafafa; max-width: 400px;">

![Treasure Box CAD Exploded View](/mirachew-website/images/exploded-labeled-view.png)

<br><em>Exploded CAD model of Treasure Box.</em>

</div>

</div>

---

## Manufacturing Process

Using Fusion 360's built-in CAM environment, I created the toolpaths and generated G-code for the Tormach 770M. I optimized for machining speed by minimizing tool changes and maintaining consistent coordinate references.

<div style="text-align: center; margin: 20px 0;">

<div style="display: inline-block; text-align: center; border: 1px solid #ccc; padding: 10px; background-color: #fafafa; max-width: 500px;">

![Treasure Box Machining](/mirachew-website/images/machining-pic.png)

<br><em>CAM setup of top and bottom pieces.</em>

</div>

</div>

**Process Summary**

1. Modeled both components parametrically in Fusion 360
2. Programmed CNC operations for roughing, drilling, chamfering, and finishing
3. Used press-fit dowel pins for precision alignment
4. Verified part dimensions using tolerance drawings and calipers
5. Initialized center-based origin setup for rotational symmetry

---

## Challenges & Learnings

- Using the center of each piece as a machining origin introduced small cumulative errors. Post-assembly facing would improve edge alignment
- Milling from 1.5" thick stock proved inefficient; future iterations could leverage waterjet-cut sheet metal for rough cuts
- Fit tolerances (FN1 vs FN2) required experimentation to balance rotation and press-fit strength

---

## Technical Drawings & Documentation

Engineering drawings were created in **Fusion 360** to define dimensional tolerances, hole fits, and GD&T callouts. These documents ensured machinability and assembly alignment between the top and bottom pieces.

<style>
.lightbox-overlay {
  display: none;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.9);
  z-index: 9999;
  cursor: pointer;
  justify-content: center;
  align-items: center;
}

.lightbox-overlay.active {
  display: flex;
}

.lightbox-image {
  max-width: 95%;
  max-height: 95%;
  object-fit: contain;
  cursor: pointer;
}

.lightbox-close {
  position: absolute;
  top: 20px;
  right: 40px;
  color: white;
  font-size: 40px;
  font-weight: bold;
  cursor: pointer;
  z-index: 10000;
}

.lightbox-close:hover {
  color: #ccc;
}

.lightbox-clickable {
  cursor: pointer;
  transition: opacity 0.2s;
}

.lightbox-clickable:hover {
  opacity: 0.8;
}
</style>

<div style="display: flex; gap: 15px; justify-content: center; margin: 20px auto; flex-wrap: wrap;">

<div style="display: inline-block; text-align: center; border: 1px solid #ccc; padding: 10px; background-color: #fafafa; max-width: 400px;" class="lightbox-clickable" onclick="openLightbox('/mirachew-website/images/drawing-bottom.png')">

<img src="/mirachew-website/images/drawing-bottom.png" alt="Treasure Box Bottom Drawing" style="max-width: 100%; height: auto;">

</div>

<div style="display: inline-block; text-align: center; border: 1px solid #ccc; padding: 10px; background-color: #fafafa; max-width: 400px;" class="lightbox-clickable" onclick="openLightbox('/mirachew-website/images/drawing-top.png')">

<img src="/mirachew-website/images/drawing-top.png" alt="Treasure Box Top Drawing" style="max-width: 100%; height: auto;">

</div>

</div>

<div id="lightbox-overlay" class="lightbox-overlay" onclick="closeLightbox()">
  <span class="lightbox-close" onclick="event.stopPropagation(); closeLightbox()">&times;</span>
  <img id="lightbox-image" class="lightbox-image" src="" alt="" onclick="event.stopPropagation()">
</div>

<script>
function openLightbox(imageSrc) {
  const overlay = document.getElementById('lightbox-overlay');
  const image = document.getElementById('lightbox-image');
  image.src = imageSrc;
  overlay.classList.add('active');
  document.body.style.overflow = 'hidden';
}

function closeLightbox() {
  const overlay = document.getElementById('lightbox-overlay');
  overlay.classList.remove('active');
  document.body.style.overflow = '';
}

document.addEventListener('keydown', function(event) {
  if (event.key === 'Escape') {
    closeLightbox();
  }
});
</script>

*Each drawing includes datums, reference dimensions, and feature control frames to ensure consistent press-fit geometry. Click on a drawing to view it in full size.*

---

## Results

- Achieved smooth rotation between top and bottom components
- Assembly alignment and CNC tolerances were slightly out of spec
- Gained hands-on understanding of real-world machinability, tolerance management, and part interfacing

---

## Technical Tools & Skills

- **Fusion 360** (CAD/CAM)
- **CNC Milling** (Tormach 770M)
- **GD&T**
- **Manual Machining**
- **Tolerance Analysis**

---

## Cost Analysis

To produce one box in house, I calculated the following Bill of Materials:

| Item/Process                                    | Price         | Quantity    | Cost     |
|:------------------------------------------------|:--------------|:------------|:---------|
| McM 7315T51 (aluminum 3"x1.5"x2ft)              | $129.48       | 1/15        | $8.63    |
| Manual Labor (Cut to ~3inch sections)           | $100 / hour   | 0.1 hours   | $10.00   |
| CNC Mill Bottom                                 | $100 / hour   | 0.75 hours  | $75.00   |
| McM 7315T15 (aluminum 3"x0.25"x2ft)             | $38.77        | 1/15        | $2.58    |
| Manual Labor (Cut to ~3inch sections)           | $100 / hour   | 0.1 hours   | $10.00   |
| CNC Mill Top                                    | $100 / hour   | 0.25 hours  | $25.00   |
| McM 98381A537 (¼" Dowel Pin ½" L)               | $4.92         | 1/25        | $0.20    |
| Shop Labor (assembly)                           | $100 / hour   | 0.1 hours   | $10.00   |
| **Total**                                       |               | **1**       | **$141.41** |

Using an online manufacturing service like Xometry for CNC machining with their standard lead time, the estimated costs are:

| Quantity to Order | Bottom Piece | Top Piece  | Total Cost  |
|:------------------|:-------------|:-----------|:------------|
| 1                 | $215         | $48        | $263        |
| 2                 | $175         | $31        | $206        |
| 3                 | $148         | $22        | $170        |
| 10                | $85          | $9         | $94         |
| 100               | $39          | $4         | $43         |

- In-house cost: ~$140 per unit
- Outsourced (Xometry, 6061-T6, no finishing process): ~$263 per single unit
- Potential savings with thinner stock and waterjet operations for top piece
- Aluminum 5052-H32 is also cheaper through Xometry

---

## Key Takeaways

This project bridged the gap between design intent and manufacturing reality. I learned how CAM setup, tolerance control, and fixture planning directly influence real-world precision and assembly performance. It strengthened my confidence in translating CAD models into functional machined parts.
