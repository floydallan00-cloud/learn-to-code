# Scientific Calculator (small)

This is a small, dependency-free scientific calculator implemented in Python.

Files:

- `sci_calc.py` - safe evaluator exposing `evaluate(expression: str, deg: bool=False)`
- `calculator.py` - interactive CLI (REPL) and one-shot runner
- `tests/test_sci_calc.py` - pytest unit tests

Quick start

Run the REPL:

```powershell
python calculator.py
```

Evaluate a single expression:

```powershell
python calculator.py "sin(pi/2) + 2**3"
```

Run tests (requires pytest available in your environment):

```powershell
# install pytest if needed
python -m pip install pytest; python -m pytest -q
```

Notes

- Trigonometric functions accept radians by default. Use `:mode deg` in the REPL
  to switch to degree-mode (or call `evaluate(expr, deg=True)` directly).
- The evaluator uses Python's AST and only permits a small whitelist of
  operations and math functions for safety.