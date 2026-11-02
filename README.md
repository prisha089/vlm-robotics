# VLM Robotics

Can a vision-language model decide where to look next?

An AI at UGA project that evaluates open and API-accessible VLMs on images of manufactured parts. Each model gets a fixed battery of questions (locate the defect, choose the next viewpoint, state its confidence) and is scored on:

- Spatial grounding accuracy
- Hallucination rate
- Confidence calibration

## Deliverables
- Evaluation harness
- Model comparison leaderboard
- Annotated question set
- Failure-mode analysis

## Setup
```bash
git clone https://github.com/prisha089/vlm-robotics.git
cd vlm-robotics
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
cp .env.example .env   # add your own API keys; never commit .env
```

## Run an evaluation
```bash
python src/run_eval.py --config configs/<name>.yaml
```
(Coming soon: harness is under construction.)

## Team
Project manager: Prisha. See CONTRIBUTING.md for how we work.

## Data
Datasets (MVTec AD, Real-IAD, etc.) are not stored in this repo. Check each dataset's license and use the download scripts in `data/`.
