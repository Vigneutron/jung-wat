# jung-wat

Word association test after C. G. Jung's method (1904–1909, published list 1910), running entirely in the browser.

**Live app: https://vigneutron.github.io/jung-wat/**

## What it does

It presents the stimulus words in order, records the first word that comes to mind and how long it took, and marks the reactions that ran longer than the subject's own median — Jung's "probable mean" rule — plus the ones that got no answer at all. That is the whole instrument: the words and the clock. Reading the sheet is a person's job.

There is no scoring, no classifier, no model, and no generated interpretation. Earlier versions of this app computed relatedness between stimulus and response with an on-device embedding model; all of that was removed in August 2026 and is not coming back.

This is not a diagnostic instrument.

## The reading

The stimulus words are recordings, not the browser reading text aloud. The word set is fixed, so each of the 250 words was recorded ahead of time in six accents — American woman and man, British woman and man, Northern English man, Scottish woman — and the accent is chosen on the setup screen. Recording rather than improvising also settles pronunciation: "lead pencil" is the metal, and "to insult" takes the verb's stress.

## Privacy

The app sends nothing to any server of ours; there is no backend. Answers and timings stay on the page and leave only as the JSON file you choose to save.

One exception, stated on the setup screen and again on the sieve screen: in microphone mode the transcription is the browser's own speech recognition, and in Chrome and Safari that sends the audio to Google's or Apple's servers. Typing mode keeps everything on the device.

## This repository

This holds the deployable build only: `index.html` at the root with `audio/` beside it, published by GitHub Pages from the `gh-pages` branch.

The source lives in `Vigneutron/psych-association-test`, and a workflow there copies `frontend/` onto `gh-pages` when main changes — **edit the app there, not here**, or the next publish will overwrite it. `.github/workflows/verify.yml` in this repository only checks that the live URL is serving the app; it does not publish.
