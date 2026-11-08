# L5 Narrow / L2 General Classification — L_CODYT5
**Platform:** Anticloud | **Tier:** TIER_6_SECURITY_EVAL | **PAX:** 27B
**IP:** USPTO pending 2026, Anticloud FZ LLE, 0-1.gg | **License:** Apache-2.0

## L5 Narrow
L_CODYT5 uses a CodeT5+-based model fine-tuned on Anticloud codebase patterns for security-focused code search and vulnerability detection. Narrow scope: Anticloud Python/Rust/CUDA code security — not general code intelligence.

## L2 General
L2 General: L_CODYT5 provides deep code understanding for security evaluation across all tier codebases. TIER_4 inference code and TIER_3 API code are both analyzed.

## PAX 27B Integration
L_CODYT5 (CodeT5+) and PAX 27B work in combination: CodeT5+ provides precise code understanding and vulnerability pattern matching; PAX provides natural language explanation and remediation guidance.

## AIOSS Audit Chain
Every code security analysis (file hash + vulnerability patterns hash + severity ranking + remediation suggestions hash) is chained: H_n = SHA3-256(H_{n-1} || entry_hash_n || timestamp_n).
Offline-verifiable, tamper-evident, zero cloud dependency.

## Regulatory / Compliance
NIST SSDF (code security analysis). OWASP ASVS.
