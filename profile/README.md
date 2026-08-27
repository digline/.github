<p align="center"><img src="https://raw.githubusercontent.com/digline/.github/main/profile/digline-wordmark.png" alt="digline" width="600"></p>

**Regression testing for LLM applications — with the baseline in your repository, not on someone's server.**

Your prompt worked on Tuesday. On Thursday it works a little less: not enough to
break, enough for a user to notice in two weeks. No ordinary test catches it,
because there is no correct output to compare against — only a better or a worse
one.

digline gives you an approved reference and, on every change, tells you whether
you are below it: which case, which check, by how much. The reference is a JSON
file in your repository, so it goes through code review and it rolls back with
`git`. No server, no account, no network call you have not configured yourself.

```console
$ digline compare --suite suite.py --run latest
2 checks got worse compared with the reference. Every case could be judged.

how-do-i-return · llm_rubric · Score fell from 1.000000 to 0.700000.
how-do-i-return · contains · Went from passing to failing (1.000000 → 0.000000).
```

```bash
uv add digline        # or: pip install digline
```

| | |
|---|---|
| **[digline](https://github.com/digline/digline)** | the engine, the CLI and the report — Apache-2.0 |
| **[on PyPI](https://pypi.org/project/digline/)** | `0.1.0`, Python 3.12+, one runtime dependency |
| **[the guide](https://github.com/digline/digline/blob/main/docs/guide.md)** | how to reason with it, in the order the problems arrive |
| **[the metrics](https://github.com/digline/digline/blob/main/docs/metrics.md)** | a card per assertion: when to reach for it, what to watch out for |
| **[the decisions](https://github.com/digline/digline/tree/main/docs/adr)** | numbered, with the reasoning, and fixed |
