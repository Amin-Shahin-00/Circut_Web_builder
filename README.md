# Circut_Web_builder



<div align="center">
  <img src="[https://upload.wikimedia.org/wikipedia/en/2/2b/Princess_Sumaya_University_for_Technology_logo.png](https://en.wikipedia.org/wiki/Princess_Sumaya_University_for_Technology)" alt="PSUT Logo" width="200"/>

  # Advanced Circuit Analyzer PRO
  **Developed by:** Amin Shahin  
  **Department:** Computer Science, Princess Sumaya University for Technology  
</div>

---

## 📌 Project Overview
The **Advanced Circuit Analyzer PRO** is a zero-dependency, browser-based Electronic Design Automation (EDA) tool. Built entirely in Vanilla JavaScript and HTML5 Canvas, it allows users to visually draw, edit, and simulate DC electrical circuits in real-time. 

Instead of relying on external physics libraries, this application features a custom-built mathematical engine that uses **Modified Nodal Analysis (MNA)** and matrix algebra to instantly calculate voltage drops and current flow across complex topologies.

## 🚀 Core Features

### 1. Custom Physics Engine (MNA Solver)
* **Matrix Algebra Backend:** Dynamically generates a netlist from the visual canvas, constructing a conductance matrix ($A \times X = Z$) and solving it via Gaussian Elimination.
* **Component Support:** Simulates Batteries (Voltage Sources), Resistors, Capacitors (DC Steady-State open circuits), and interactive Switches.
* **Ohm's Law Integration:** Automatically calculates the exact Amperes flowing through every branch and renders directional gold arrows on the UI to visualize electron flow.

### 2. Professional CAD Interface
* **Infinite Workspace:** Features an interactive camera matrix allowing users to right-click and pan infinitely, or use the scroll wheel to zoom in and out of massive schematics.
* **Voltage Heatmaps:** Wires dynamically change color based on the simulation results (Red for positive voltage, Blue for negative, White for ground).
* **Command Design Pattern:** Includes a full `Ctrl+Z` (Undo) and `Ctrl+Y` (Redo) state-history stack.

### 3. Data Persistence & Export
* **Local Storage:** Users can seamlessly Save and Load their entire circuit layouts directly to the browser's local memory.
* **SPICE Compilation:** A built-in compiler translates the visual graph into standard SPICE text syntax, the industry standard format used by professional electrical engineers.

## 🛠️ Technical Stack
* **Frontend:** HTML5, CSS3, Vanilla JavaScript (ES6+).
* **Graphics:** HTML5 `<canvas>` API (Context 2D) using custom translation, rotation, and scaling matrices.
* **Architecture:** Object-Oriented Programming (OOP) with an explicit separation between the UI layer, the state machine, and the mathematical solver.
* **Dependencies:** Zero. The engine was written from scratch.

## 📖 How to Use

1. **Draw a Circuit:** Select a tool (Wire, Resistor, Battery, etc.) from the floating toolbar. Click and drag on the dotted grid to place components. 
2. **Edit Values:** Double-click any Resistor, Battery, or Capacitor to input a specific value (Ohms, Volts, or Microfarads). Double-clicking a Switch will toggle it open or closed.
3. **Simulate:** Click **Run Simulation**. The engine will calculate the nodal voltages, display them in neon green, and overlay current-flow arrows.
4. **Navigate:** Right-click and drag to pan the camera. Use the mouse wheel to zoom. 
5. **Erase & Undo:** Use the Eraser tool to surgically remove components, or use the Undo/Redo buttons to step backward through your drawing history.
6. **Export:** Click **SPICE** to generate a text-based netlist of your current visual design.

---
*Developed for educational and demonstration purposes.*
