# Harness Diagnostic Matrix Skill

A runnable workflow skill for generating evidence-backed diagnostic matrix diagrams for any harness.

This repository is owned by Runyuan Wang (`9s5bz2jvd2-lang`). It contains a generic LingTai workflow bundle under:

```text
workflows/harness-diagnostic-matrix/
```

## Mandatory self-test

Any agent using the skill must first run:

```bash
cd workflows/harness-diagnostic-matrix
python scripts/selftest_harness_matrix.py
```

Expected output begins with:

```text
SELFTEST PASS: rendered selftest_matrix.html from a fresh arbitrary harness input (2 rows).
```

If self-test fails, stop. Do not produce a final diagnostic matrix.

## Render the example

```bash
cd workflows/harness-diagnostic-matrix
python scripts/render_harness_matrix.py examples/example_harness_matrix.json examples/example_harness_matrix.html
```

The matrix is diagnostic-only: symptoms, system sites, evidence, likely causes/problems, differentials, missing evidence, severity, and confidence. It does not prescribe fixes or implementation plans.
