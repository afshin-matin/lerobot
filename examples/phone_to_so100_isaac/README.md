# phone_to_so100_isaac

Purpose
- Alternative to `examples/phone_to_so100`.
- Uses the "isaac" variant of the phone preprocessing & mapping (alternate phoneme normalization and alignment).
- Demonstrates swapping a phoneme mapping and minor audio preprocessing while reusing the main conversion pipeline.

Differences vs `phone_to_so100`
- phoneme set: "isaac" phoneme normalization rules (see config.yaml).
- optional additional audio pre-processing (pre-emphasis / normalization).
- provides a sample mapping JSON and a minimal runnable script.

Files
- `config.yaml` — isaac-specific mapping and parameters
- `run_inference.py` — minimal runnable example that loads audio or phone sequence and converts to so100
- `mappings/isaac_phone_to_so100.json` — sample phoneme->so100 mapping
- `requirements.txt` — minimal Python dependencies

Usage
1. Create a virtualenv and install requirements:
   python -m venv venv && source venv/bin/activate
   pip install -r requirements.txt
2. Edit `config.yaml` to point to your model/save locations if needed.
3. Run:
   python run_inference.py --input my_audio.wav --output output.json