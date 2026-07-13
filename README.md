# Non-hyperbolic knot list

The seven non-hyperbolic prime-knot types with at most 11 crossings used by
this organization, together with invariant records for both chiral spellings.
The classification source is the
[Regina knot and link census](https://regina-normal.github.io/data.html).

## Files

- `data/non_hyperbolic_knot_list.txt` contains seven base knot names.
- `data/non_hyperbolic_HOMFLY-PT.txt` contains 14 HOMFLY-PT/name records,
  including mirror-prefixed names.
- `data/non_hyperbolic_khovanov.txt` contains the corresponding 14 Khovanov
  homology/name records.

Invariant records use `[VALUE|KNOT_NAME]`. The mirror entries are retained
because HOMFLY-PT and Khovanov data may encode chirality even though
hyperbolicity itself does not.

## Usage

```python
from pathlib import Path

non_hyperbolic = set(
    Path("data/non_hyperbolic_knot_list.txt")
    .read_text(encoding="utf-8")
    .splitlines()
)
```

No external software is required to consume the committed files. This
repository does not attempt to assign a geometric volume to non-hyperbolic
knots.

