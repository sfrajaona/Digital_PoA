# DPoA_in_PRISM_games


**DPoA_in_PRISM_games** is a PRISM games modelling of a digital power of
attorney protocol.

---

## Requirements

- Java 9 or higher
- Compatible OS: Windows, Linux, or macOS
- PRISM-games installed. See [https://www.prismmodelchecker.org/games/download.php](https://www.prismmodelchecker.org/games/download.php).

---

## Usage with PRISM-games GUI

### 1. Launch the PRISM-games GUI

* **Linux/macOS**: Run `bin/xprism` from the PRISM-games directory.
* **Windows**: Double-click the PRISM-games shortcut.

---

### 2. Load the Model File

* In the GUI, go to the **Model** menu → **Open model**.
* Select the file: `modelSimple.prism`.
* The model should appear in the right pane. If parsed successfully, a checkmark ✅ will appear next to the model name in the left pane.
* Confirm that the model type is shown as **csg** (concurrent stochastic game).

---

### 3. Load the Property File

* In the GUI, go to the **Properties** menu → **Open properties list**.
* Select the file: `goalsModelSimple.props`.

---

### 4. Verify a Property

* Right-click on any listed property and select **Verify**.
* Use the bottom tabs to switch between:

  * **Model**
  * **Properties**
  * **Simulator**
  * **Log**

---
## Contact
Contact the maintainer: sfrajaona@gmail.com

