# Inconel 718 Bolted Joint K-Factor Characterization

**Stoke Space | June 2026 - August 2026**

During my internship at Stoke Space, I characterized the K-factor (nut factor) for the company's Inconel 718 bolted joints. Inconel 718 is widely used across the aerospace industry for high-load, high-temperature components, and the K-factor is what links the torque a technician applies to the clamp load the joint actually sees. An inaccurate K-factor means joints that are under- or over-preloaded, even when every bolt is torqued "to spec."

I owned the project end to end: researching which joints mattered, designing test plates and a test plan, refining the assembly method to match company standards and reduce error, running every test, and analyzing the results of over 500 tests.

---

## Research

Before designing any hardware, I worked to understand how these joints were actually being specified and assembled, not just how they appeared on paper. I cross-referenced the standard hardware options with real usage on the rocket to narrow down which joint configurations were worth testing.

- **Surveying responsible engineers:** Interviewed REs across the company to learn which joints they relied on and where they had seen problems.
- **Watching technician installations:** Observed techs assembling joints on the floor to capture real-world technique, tooling, and sequence.
- **Examining failures:** Reviewed past joint failures to identify which variables were most likely driving scatter in preload.

This research directly shaped the test setup. It surfaced variables I would not have controlled for otherwise, and made sure the test conditions reflected how hardware is really built.

<!-- TODO: optionally add 2-4 specific variables you controlled for (e.g. lubrication, washer type, reuse, torque rate). Concrete examples here show detail-orientation better than a full test plan. -->

---

## Test Approach

I designed custom test plates and a structured test plan to isolate the K-factor while holding everything else constant. As results came in, I iterated on the assembly method, tightening the procedure to align with company standards and remove sources of error, until the data converged on an accurate and repeatable value.

<!-- TODO (optional): link a sanitized one-page test plan summary here, e.g. [View test plan summary](/mirachew-website/kfactor_test_plan.pdf) -->

---

## Results

<div style="text-align: center; margin: 20px 0;">

<div style="display: inline-block; text-align: center; border: 1px solid #ccc; padding: 10px; background-color: #fafafa; width: 760px; max-width: 100%;">

<img src="/mirachew-website/images/kfactor_placeholder.svg" alt="Illustrative torque vs. preload plot showing reduced scatter after method refinement" style="width: 100%; height: auto;">

<br><em>Illustrative representation of the torque-preload data (not to scale, no real values). Refining the assembly method narrowed the error band and converged on a more accurate, precise K-factor.</em>

</div>

</div>

The characterized K-factor helped the company track down the root cause of several major mechanical failures and correct them. The testing also uncovered issues beyond the K-factor itself, including inconsistencies in technician assembly methods and manufacturing differences between parts.

---

## My Role & Contributions

- **Research:** Surveyed REs, observed technician installations, and reviewed failures to define test scope.
- **Test Design:** Designed test plates and wrote the test plan to isolate the K-factor.
- **Method Development:** Refined the joint assembly procedure to match company standards and reduce error.
- **Testing:** Carried out all testing, over 500 individual tests.
- **Analysis:** Analyzed the full dataset, fit results, and quantified uncertainty to arrive at the final K-factor.

---

## Key Results

- Characterized the K-factor for Inconel 718 bolted joints across standard hardware used on the vehicle.
- Ran and analyzed over 500 tests, significantly narrowing the uncertainty in the K-factor.
- Helped identify and fix the root causes of major mechanical failures.
- Exposed variation in technician assembly methods and manufacturing differences.

---

## Key Challenges & Learnings

The biggest lesson from this project was how much every small detail in a test affects the result. Changes that seemed insignificant showed up clearly in the data, which made consistency in setup and execution essential.

It also showed me the value of the research I did before testing. Talking to REs, watching technicians, and studying failures is what allowed me to design a test that captured the variables that actually mattered. Going forward, I'll continue to invest that upfront effort, deciding deliberately when to narrow a test plan down and when to expand it to get closer to the truth.

- Designing a test that isolates one variable in a system with many interacting factors
- Maintaining consistency across hundreds of repeated tests
- Translating test findings into actionable fixes for both design and assembly

---

## Technical Tools & Skills

- **Bolted Joint Design & Analysis**
- **Test Plan Development**
- **Torque-Tension Testing**
- **Data Analysis & Uncertainty Quantification**
- **Root Cause Investigation**
- **Cross-Team Communication**
