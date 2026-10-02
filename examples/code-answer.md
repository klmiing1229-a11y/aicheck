# Example: code before you run it

**User:** aicheck
> To drop duplicate rows in pandas and keep the newest, sort first:
> `df.sort_values("date").drop_duplicates(subset="id", keep="last", inplace=True)`
> This works in every pandas version.

**aicheck:**

**Checking:** a one-line pandas snippet for de-duplicating rows
**Used for:** not stated, assumed a script you'll run on real data
**Stakes:** medium: a silent bug changes your data without an error

| # | Claim | Risk | Check it by |
|---|---|---|---|
| 1 | The chained line changes `df` | 🔴 | Run it on a 3-row test table and print `df` after. `inplace=True` on the sorted copy leaves the original `df` unsorted and un-deduplicated |
| 2 | "Works in every pandas version" | 🟡 | Check `pd.__version__` and the `drop_duplicates` page in the docs for that version |
| 3 | `keep="last"` keeps the newest row after sorting by date | 🟢 | Follows from the sort order. Confirm in the same 3-row test |

**Check first:** #1, because the line runs without an error and does nothing to `df`.
**Safe to use as-is:** the approach (sort, then keep last) is sound.

Next? (check it for me / fix the answer / done)
