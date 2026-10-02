# memory-game

A historical grid-based matching-card exercise adapted from
[kubowania/memory-game](https://github.com/kubowania/memory-game). This repository
records tutorial learning, with the upstream attribution preserved.

## Preview and play

With Python 3, run from the repository root:

```sh
python -m http.server 8000 --bind 127.0.0.1
```

Open `http://127.0.0.1:8000` and stop with Ctrl+C. Click two cards to compare them;
the page reports matched pairs and guesses. There are six pairs. Refresh to
reshuffle and restart. No npm installation, build or environment configuration
is required.

[`app.js`](app.js) creates and shuffles the cards and checks matches after a short
delay. [`index.html`](index.html), [`style.css`](style.css) and `images/` provide
the interface and card artwork.

## Known limitations

The current handler does not lock input during the comparison delay or prevent
choosing the same card twice. Keyboard controls are not implemented, and shuffle
uses a random sort comparator. No automated suite or CI workflow is committed.
This source review did not certify browser gameplay. A focused fix should verify
those edge cases and preserve the [MIT license](LICENSE), images and tutorial
attribution.
