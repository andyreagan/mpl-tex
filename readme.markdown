Testing matplotlib and latex together, such that the fontsize in a matplotlib figure with pdf backend can have that same fontsize in an actual document.

Setting the mpl figsize to the actual figure width in the document does not work (captions too small), so I ended up with a trail and error solution.
I can now use this solution to fix up figures for a paper (ended up being 8.5 inches for a one column revtex document).

The best way that I can figure out to test this is to just render each.
In `revtex-preprint.tex`, the python scripts themselves are contained.

```pdflatex -shell-escape revtex-preprint```

creates `revtex-preprint{1..6}.py` and runs them.
Seems to take a really long time to run them.

Result: something like 3.6in and 8.45 for two column, one column, respectively.







