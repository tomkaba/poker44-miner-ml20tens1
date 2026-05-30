# ml20tens1

Minimal release repository for Poker44 miner runtime scoring.

This repository is a standalone miner variant prepared for production rollout with the gen20_tens1_7k_vote101_hardened TorchScript scorer, prod-like runtime preprocessing, and the default 0.5 decision threshold.

## Quick start

```bash
git clone https://github.com/tomkaba/poker44-miner-ml20tens1.git
cd poker44-miner-ml20tens1
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
pip install -e .
```

## Run Miner

```bash
python neurons/miner.py
```

or legacy wrapper:

```bash
./start_miner.sh HOTKEY_ID[,HOTKEY_ID2,...]
```

## Implementation

- Launcher: start_miner.sh
- Scorer entrypoint: poker44/miner_heuristics.py
- Entry point: neurons/miner.py
- Runtime model: weights/gen20_tens1_7k_vote101_hardened.ts

Base release lineage: ml20tens1 with the gen20_tens1_7k_vote101_hardened artifact and decision threshold kept at the default 0.5.

Manifest implementation SHA256 is computed from:

- start_miner.sh
- weights/gen20_tens1_7k_vote101_hardened.ts
- neurons/miner.py
- poker44/__init__.py
- poker44/base/miner.py
- poker44/base/neuron.py
- poker44/miner_heuristics.py
- poker44/utils/config.py
- poker44/utils/misc.py
- poker44/utils/model_manifest.py
- poker44/validator/synapse.py
