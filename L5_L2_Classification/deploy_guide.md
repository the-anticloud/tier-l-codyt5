# Deploy Guide — L_CODYT5
**Tier:** TIER_6_SECURITY_EVAL | **Stack:** Python 3.11, CodeT5+ (fine-tuned), PAX 27B, AIOSS_FORMAT
**Air-gap capable after initial setup.**

## Prerequisites
Python 3.11+, CodeT5+ fine-tuned weights (~3GB), PAX 27B. T4 GPU.

## Environment
T4 GPU. CodeT5+ weights: ~3GB VRAM. Compatible with PAX 27B on same T4.

## AIOSS Integration
```bash
aioss init --module L_CODYT5 --output ./l_codyt5.aioss
aioss append --chain ./l_codyt5.aioss --payload ./output.bin --module L_CODYT5
aioss verify --chain ./l_codyt5.aioss
```

## Air-Gap Setup
```bash
pip download -r requirements.txt -d ./wheels/
pip install --no-index --find-links ./wheels/ -r requirements.txt
```

## PAX 27B Harness Wiring
```python
from anticloud_pax import PAXHarness
harness = PAXHarness(
    model_path="./pax-27b-q4.gguf",
    module="L_CODYT5",
    aioss_chain="./L_CODYT5.aioss",
    classification="L5_NARROW_L2_GENERAL"
)
result = harness.process(input_data)
```

## Verification
```bash
aioss verify --chain ./L_CODYT5.aioss --verbose
python -m L_CODYT5.tests.smoke
```
