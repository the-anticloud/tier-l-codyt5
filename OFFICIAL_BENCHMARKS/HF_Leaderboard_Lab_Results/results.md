# HF_Leaderboard_Lab_Results

**Project:** `L_CODYT5`  
**Tier:** `TIER_6_SECURITY_EVAL`  
**Slug:** `Salesforce/codegen`  
**Commit:** `ec21c93bda19`  
**Run:** `2026-09-30T15:07:07.146295+00:00`  

## Isolation Environment

| Field | Value |
| ----- | ----- |
| Platform | `win32` |
| Python | `3.12.10` |
| HF model | `distilbert-base-uncased` |
| HF load time | `4.42s` |
| Inference device | `cpu` |

## Results

**Framework:** [HuggingFace Open LLM Leaderboard (proxy via distilbert-base-uncased)](https://huggingface.co/docs/leaderboards/en/open_llm_leaderboard/archive)

**Model used:** `distilbert-base-uncased`

### Inference Latency (Classification)

| Metric | Value |
| ------ | ----- |
| Avg latency | **39.43 ms** |
| Min latency | 34.98 ms |
| Max latency | 42.99 ms |
| Samples | 5 |

### Real Tokenization Results

| Field | Value |
| ----- | ----- |
| Token count | **37** |
| Tokenization latency | 1.0 ms |
| Classification label | `LABEL_0` |
| Classification score | 0.583 |
| Classification latency | 64.0 ms |
| Status | **PASS** |

**Input text tokenized:**
```
L_CODYT5 (Salesforce/codegen) — 26 files, 2113 source lines, licence Apache-2.0, primary language ['Python']
```

**First 20 tokens:**
```
['[CLS]', 'l', '_', 'cody', '##t', '##5', '(', 'sales', '##force', '/', 'code', '##gen', ')', '—', '26', 'files', ',', '211', '##3', 'source']
```

> Full MMLU/HellaSwag/TruthfulQA/ARC/Winogrande/GSM8K require dedicated GPU.
> These results are CPU inference proxy metrics using distilbert-base-uncased.

---
_Anticloud Benchmark Suite — isolation log — 2026-09-30T15:07:07.146295+00:00_