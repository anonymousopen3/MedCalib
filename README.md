# MadCalib Verified Research Implementation

This package contains the streamlined, audited scripts from the **MedCalib** codebase (`claib.py` and `claib_slake.py`). 

## 📂 Contents
- `engine.py`: consolidated behavioral probing logic.
- `generate.py`: inference and signal logging module (produces JSONs).
- `metrics.py`: score processor and calibration fusion (produces Table 1 results).

## 🚀 How to Reproduce
1. **Signal Generation (JSON only, no metrics)**:
   ```bash
   python generate.py --model [ID] --dataset PMC-VQA_test --output [PATH].json
   ```
2. **Result Verification**:
   ```bash
   python metrics.py [PATH].json
   ```

## 🏮 Protocol
This implementation follows the exactly verified **Fair Alignment** protocol:
- **30% Calibration Split** (Training the Fusion Layer)
- **70% Evaluation Split** (Testing Reliability)
- **Seed 42** for deterministic reproduction.
