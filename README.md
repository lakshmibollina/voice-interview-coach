# Voice Interview Coach

Real-time voice practice: you speak an answer, it transcribes, gives feedback, and talks back.

## Pipeline

Mic → Whisper (speech-to-text) → LLM feedback → TTS → speaker, over WebSockets.

## Production focus

- End-to-end latency budget, decomposed per stage
- Graceful degradation when a stage is slow
- Timeout handling

## Also here

**Live log anomaly explainer** — streams server logs and explains spikes in plain English.
Pipeline: log stream → anomaly detection → LLM summary.

## Run it

```bash
pip install -r requirements.txt
uvicorn src.main:app --reload
```
