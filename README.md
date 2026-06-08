# ⚙️ Kinematic Mechanism Synthesis for Guided Rigid Body Motion


An elegant computational solver implemented in Python (Google Colab) to synthesize a mechanism restricted to revolute and prismatic joints. The system guides a partial circular body through three highly constrained precision states and executes a quick-return motion.

---
📑 Problem Statement

The objective of this project (Stage II) is to synthesize a mechanism that handles the precise positional layout shown below:

![Problem Statement Geometry]
<img width="753" height="508" alt="Screenshot 2026-06-08 at 7 33 51 PM" src="https://github.com/user-attachments/assets/4ccdf97d-bc4e-4835-b702-4e8357af5a4f" />

 📐 Kinematic Constraints & Rules:
* **Geometry:** A partial circular object with a radius of **5 cm**.
* **Path Trajectory:** The object must move sequentially from orientation **A → B → C**, and then return to **A** exactly **twice as fast** (Time Ratio $TR = 2$).
* **Center Motion Restriction:** The geometric center of the object is strictly constrained to **zero horizontal motion**. It transitions exclusively downward along a single vertical vector.
* **Displacements:** 
  * In **B**, the center moves downwards by **5 mm**, making the body perfectly symmetric about the fixed horizontal line passing through the center.
  * In **C**, the center moves further down to a total vertical displacement of **15 mm** relative to position A.
* **Joint Selection:** The mechanism must exclusively employ **revolute (R)** or **prismatic (P)** joints.
* **Parametric Scalability:** The entire programmatic solver is generic, allowing it to seamlessly handle any changes to the default numerical input metrics ($5\text{ cm}$, $5\text{ mm}$, and $15\text{ mm}$).

---

## 🛠️ Project Structure

```text
├── machine_design.ipynb   # Main Google Colab notebook (Cleaned, no-output file)
├── README.md              # Project documentation and problem formulation
└── Screenshot 2026-06-08 at 7.13.39 PM.png



screenshot of the simulation:
<img width="961" height="546" alt="Screenshot 2026-06-08 at 7 42 06 PM" src="https://github.com/user-attachments/assets/b1a3ba85-9f31-46ef-a6bc-3c88cb7adf77" />
