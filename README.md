# Qubit Quest: Quantum Vault

## Project Metadata

* **Project Title:** `Qubit Quest: Quantum Vault`
* **Team Name:** `QUANTAREALM`
* **Chosen Track:** `Track 1: Quantum Games & Interactive Puzzles`
* **Video Presentation Link:** (https://drive.google.com/drive/folders/1V7yQVyYkma-NkgY2r4w0073T6M7Fudh1?usp=drive_link)
* **Live Demo Timestamp in Video:** `[00:21]`

### Team Members (Max 4 members)

| Name | Email | GitHub Username |
| :--- | :--- | :--- |
| SIVAJAGATHEESH V | `sivajagatheeshv@gmail.com` | `sivajagatheeshv` |

---

## 1. Project Overview & Motivation

* **Summary (3–4 sentences):**  
  Qubit Quest: Quantum Vault is an educational puzzle game where players solve clues to identify the correct vault while managing scores, lives, and streaks across increasing difficulty levels. The project explores Grover's search algorithm using Qiskit and the Qiskit Aer simulator. The quantum circuit demonstrates superposition, oracle-based target marking, diffusion, and measurement. The goal is to make quantum computing concepts more interactive through game design.

* **Why this problem / game?**  
  Quantum computing can be difficult for beginners to understand through theory alone. I chose a puzzle game to make learning more interactive and engaging. By combining vault-solving gameplay with a Grover-style quantum circuit demonstration, the project introduces the basic idea of quantum search in a beginner-friendly way.

---

## 2. Quantum Architecture & Mechanics

* **Core Quantum Principles Used:**  
  Superposition using Hadamard gates, phase marking through an oracle, amplitude amplification using the diffusion operator, and measurement.

* **How the Quantum Circuit is Integrated:**  
  The game presents clues that help players identify the correct vault. The quantum demonstration explores Grover's search algorithm for finding a marked target among possible states. Qiskit and Qiskit Aer are used to build and simulate the circuit. The target state is predefined in the oracle, so the notebook demonstrates the algorithm's concept rather than providing a quantum advantage within the game's runtime.

* **Circuit Details:**
  * **Number of Qubits:** `4`
  * **Key Gates Used:** Hadamard (H), oracle phase-marking operations, diffusion operations, and measurement.
  * **Primitives Used:** Qiskit Aer simulator.
  * **Other Technologies Used:** Python, Pygame, Qiskit, Qiskit Aer, and Jupyter Notebook / Google Colab.

```python
# Representative Grover-style circuit outline
from qiskit import QuantumCircuit

qc = QuantumCircuit(2, 2)

# Create superposition
qc.h([0, 1])

# Oracle and diffusion operations
qc.measure([0, 1], [0, 1])
```

---

## 3. Repository Structure & How to Run

### Project Structure

```text
├── README.md
├── requirements.txt
├── main.py
├── notebooks/
│   └── quantum_vault_demo.ipynb
└── references/
```


### Installation & Execution Instructions

**Environment Recommendation:** Use a fresh Python virtual environment or Google Colab for the quantum notebook.

1. **Clone the repository:**

```bash
git clone [your-repo-url]
cd [your-repo-folder]
```

2. **Install dependencies:**

```bash
pip install -r requirements.txt
```

If `requirements.txt` is not available, install the required libraries:

```bash
pip install pygame qiskit qiskit-aer
```

3. **Run the project / demo:**

```bash
python main.py
```

To explore the quantum circuit, open `notebooks/quantum_vault_demo.ipynb` in Jupyter Notebook or Google Colab and run its cells.

---

## 4. Implementation Walkthrough & Live Demo

* **Walkthrough of Gameplay / Optimization Pipeline:**  
  1. The player opens the game and views the available vault puzzle.
  2. The player uses the displayed clues to identify the correct vault.
  3. The game tracks the player's score, remaining lives, and streak.
  4. The difficulty increases as the player progresses.
  5. The quantum demonstration uses Qiskit and Qiskit Aer to explore a Grover-style search circuit. Hadamard gates create superposition, the oracle marks the target state, the diffusion operation amplifies its probability, and measurement produces the observed outcomes.

* **Key Screenshots / Terminal Output:**  
  Add screenshots of the running game, puzzle interface, and quantum circuit or notebook output here.

**Video demonstration:**(https://drive.google.com/drive/folders/1V7yQVyYkma-NkgY2r4w0073T6M7Fudh1?usp=drive_link)

---

## 5. Classical vs. Quantum Comparison

* **Classical Baseline / Counterpart:**  
  A classical search can examine candidate vaults one by one until it finds the correct answer. The game's clue-based solving process provides a classical gameplay counterpart. The quantum notebook separately demonstrates Grover's search algorithm using a predefined target.

* **Comparative Analysis:**  
  Grover's algorithm can reduce the number of oracle queries for an unstructured search under suitable conditions, compared with classical unstructured search. However, this project does not include sufficient controlled experiments to establish a measured performance advantage. The quantum circuit is an educational simulation, and its target state is predefined in the oracle.

---

## 6. Performance, Results & Limitations

* **Key Results & Observations:**  
  The project provides a playable puzzle game with clues, scoring, lives, streaks, and increasing difficulty. It also demonstrates the main stages of a Grover-style quantum search circuit using Qiskit and Qiskit Aer. The combination offers a beginner-friendly way to explore the relationship between quantum computing and game design.

* **Critical Reflection on Limitations:**  
  The quantum circuit runs on a simulator rather than real quantum hardware. The target state is predefined, and the quantum demonstration is not directly integrated into the game's runtime decision-making. Larger circuits require more computational resources, and real quantum hardware can be affected by gate errors, noise, and decoherence. Further experiments with a fair classical baseline and multiple search sizes are needed before drawing performance conclusions.

---

## 7. References & Acknowledgments

* [Qiskit Documentation](https://docs.quantum.ibm.com/)
* [Qiskit Learning Resources](https://learning.quantum.ibm.com/)
* [Qiskit Aer Documentation](https://qiskit.github.io/qiskit-aer/)
* **Acknowledgments:** This project was developed for Qiskit Fall Fest 2026. Thanks to the organizers and the open-source quantum computing community for providing learning resources.
