
# Flowchart Example

Can be viewed here: https://gss-cogs.github.io/trace-flowchart-examples/index.html

What we're aiming at is to log out information via the TransformTrace class. To generate this flowchart of what data has been extracted, from where and what post prossesing has taken place.

Basically, a simple overview with optional complexity (and have it created automatically).


# Types (for want of a better term)

* Pipeline - the name of the pipeline, our starting node (only ever one of these)
* Landing Page - a landing page for a pipeline (one or more per pipeline)
* Distribution - a file taken from a landing page (one of more per landing page)
* Table - a "table" for a spreadsheet, a single csv or something pieced together from one of more of them (one of more per distribution).
* PMD - the uploaded output (only ever one of these)

# This Repo

* I've mocked up the input data as `trace.json` (this isn't how the TransformTrace is logging things at the moment but it's all data it has access to and could). 
* `flowchart.ttl` is build from `trace.json` (you could/should just output ttl directly from the trasformTrace if we go down this route).
* `index.html` template that uses `flowchat.ttl` to render the flowchart page you end up looking at.

# Running Locally

If you want to tweak you'll need to change `trace.json` then run `python3 makettl.py`. To view your new flowchart:
* in the terminal run a local file server `python3 -m http.server --bind 127.0.0.1 3333`
* then browse to `http://127.0.0.1:3333/index.html`
