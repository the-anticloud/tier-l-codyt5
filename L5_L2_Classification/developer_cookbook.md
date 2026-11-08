# Developer Cookbook — L_CODYT5
**Stack:** Python 3.11, CodeT5+ (fine-tuned), PAX 27B, AIOSS_FORMAT
**Domain:** CodyT5: code search and security analysis using T5-based code models for Anticloud

## Security code analysis
```python
from l_codyt5 import CodyT5Analyzer

analyzer = CodyT5Analyzer(
    codet5_model="./anticloud_codet5_security.pt",
    pax_model="./pax-27b-q4.gguf",
    aioss_chain="./codyt5.aioss"
)

result = analyzer.analyze_security(
    file_path="E:/fenta/Downloads/The Anticloud/TIER_4_INFERENCE_AGENTS/K_SGLANG/engine.py"
)
print(f"Vulnerabilities: {len(result.findings)}")
for finding in result.findings:
    print(f"  [{finding.severity}] {finding.cwe}: {finding.description}")
    print(f"  Fix: {finding.pax_fix}")
```

## AIOSS Chain Append
```python
import hashlib, time

def aioss_append(chain_path, payload: bytes, module_id: str):
    entry_hash = hashlib.sha3_256(payload).digest()
    ts = int(time.time_ns()).to_bytes(8, 'big')
    with open(chain_path, 'rb') as f:
        f.seek(-32, 2); prev_hash = f.read(32)
    new_hash = hashlib.sha3_256(prev_hash + entry_hash + ts).digest()
    with open(chain_path, 'ab') as f:
        f.write(ts + entry_hash + new_hash)
    return new_hash.hex()
```
