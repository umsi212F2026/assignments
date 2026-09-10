# Format for `results.json`

`analysis.py` must write a file called `results.json` in the top level of the
`ps1-data-analysis` folder, in exactly this shape. It is read by a program, so the structure
matters more than it usually would.

Give this file to your coding agent.

## Rules

- Ids are **numbers**, not strings. `1234`, not `"1234"`.
- Ratings and scores are **numbers**, not strings. `4.123`, not `"4.123"`. Values are compared
  with a tolerance of 0.001, so do not worry about how many decimal places you keep.
- Every list is **sorted**, best first, by the quantity that task ranks on.
- Where entries **tie** on that quantity, their order relative to each other does not matter.
- `task1` holds 10 entries. `task2` holds 3. Both `task3` lists hold 5.
- No extra top-level keys. Extra keys inside an entry are ignored.

## Shape

**Every value below is invented.** The ids, titles, counts and scores are placeholders chosen to
show the shape. None of them is an answer, and none of them is a number you should expect to see
in your own output. If one of yours happens to match, that is a coincidence and not a check.

```json
{
  "task1": [
    {
      "movieId": 1234,
      "title": "Example Movie, The (1998)",
      "rating_count": 87,
      "average_rating": 4.123
    }
  ],

  "task2": [
    {
      "userId": 42,
      "genre_count": 9
    }
  ],

  "task3": {
    "naive": [
      {
        "users": [11, 22],
        "movies_in_common": 37
      }
    ],
    "alternative": {
      "measure": "One sentence saying what you computed, precise enough that someone could implement it from this description alone.",
      "pairs": [
        {
          "users": [33, 44],
          "score": 0.42
        }
      ]
    }
  }
}
```

Each list above shows one entry as an example. Yours hold the number of entries given in the
rules.

## Notes

**`users` is a two-element list.** Order within the pair does not matter.

**`score` is whatever your alternative measure produces**, on whatever scale it produces it. It is
not checked against a formula, because it is your measure. Report it as you computed it.

**`title` comes from `movies.csv`**, unchanged, including the year and the odd comma placement
that file uses.
