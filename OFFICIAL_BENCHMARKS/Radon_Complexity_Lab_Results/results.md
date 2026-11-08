# Radon_Complexity_Lab_Results
**Project:** `L_CODYT5` | **Status:** `PASS` | **Run:** `2026-09-30T17:14:20.030944+00:00`

**Framework:** [Radon — Cyclomatic Complexity & Maintainability Index](https://radon.readthedocs.io/)

## Key Metrics

- **files_analyzed:** `7`
- **average_complexity:** `{'grade': 'A', 'score': 2.9642857142857144}`
- **complexity_grade:** `A`
- **complexity_score:** `2.9642857142857144`
- **mi_output:** `E:\fenta\Downloads\The Anticloud\TIER_6_SECURITY_EVAL\L_CODYT5\UPSTREAM\_anticloud_egress.py - A (79.55)
E:\fenta\Downlo`

## Raw Output (first 50 lines)
```
E:\fenta\Downloads\The Anticloud\TIER_6_SECURITY_EVAL\L_CODYT5\UPSTREAM\_anticloud_egress.py
    F 38:0 _is_frontier - A (4)
    F 43:0 guarded_connect - A (4)
    F 61:0 install - A (3)
    F 33:0 is_offline - A (1)
    C 29:0 EgressDenied - A (1)
E:\fenta\Downloads\The Anticloud\TIER_6_SECURITY_EVAL\L_CODYT5\UPSTREAM\codegen1\benchmark\mtpb_exec.py
    F 330:0 check_equivalence - C (15)
    F 404:0 eval_problems - C (13)
    F 221:0 test_try_rewrite_ast_with_print - B (7)
    F 152:0 read_jsonl - A (5)
    F 377:0 estimate_pass_at_k - A (4)
    F 35:0 reliability_guard - A (3)
    F 478:0 main - A (3)
    F 129:0 cast - A (2)
    F 146:0 write_jsonl - A (2)
    F 170:0 rewrite_ast_with_print - A (2)
    F 213:0 try_rewrite_ast_with_print - A (2)
    F 261:0 do_exec - A (2)
    F 275:0 test_print_stack_exec - A (2)
    F 300:0 overload_builtin_print - A (2)
    C 108:0 print_time - A (2)
    F 120:0 set_env - A (1)
    F 124:0 set_seed - A (1)
    F 135:0 gs_copy - A (1)
    F 318:0 time_limit - A (1)
    M 109:4 print_time.__init__ - A (1)
    M 112:4 print_time.__enter__ - A (1)
    M 116:4 print_time.__exit__ - A (1)
    C 313:0 TimeoutException - A (1)
E:\fenta\Downloads\The Anticloud\TIER_6_SECURITY_EVAL\L_CODYT5\UPSTREAM\codegen1\benchmark\mtpb_sample.py
    F 214:0 sample_completions - C (18)
    F 158:0 truncate - B (8)
    F 194:0 create_problem_set - A (5)
    F 67:0 write_jsonl - A (3)
    F 51:0 set_seed - A (2)
    F 61:0 cast - A (2)
    F 83:0 create_model - A
```

---
_Anticloud Independent Benchmark — 2026-09-30T17:14:20.030944+00:00_