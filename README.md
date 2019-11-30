# venice_directions_nanogenmo
*Crappy code to generate a #nanogenmo based on directions from my Airbnb host. Tracery + GPT2 small, using data from Open Street Maps and flickr pics.*

### Background Strory

When I was in Venice in mid-November, my AirBnB host tried to give me directions to some places he liked using a paper map.  Every time he circled a square and paused, I thought, "This is where it is," and it wasn't.  The directions kept going on and on and were really complicated because Venice is complicated (or was, without mobile GPS).  I decided to recreate the experience of listening to him.

### Some Tech Details

This project used Tracery grammars ([pytracery](https://github.com/aparrish/pytracery) from Allison Parrish), downloaded data on canals and roads from Open Street Map (wow that was non-obvious), plus a small GPT2 model I ran locally, trained on historic and recent guidebooks/ histories of Venice (Gutenberg books plus a couple I purchased). The small model GPT2 output is much worse than from the medium or larger models, but I couldn't get those to run in "real time" on my Mac and had too many issues setting them up remotely in the few days I had for this.  Gotta generate that word count!!!!  I'll add a punctuation-cleaned version later.  (Biggest differences in the models: the small model has much worse syntax, more repetition, less successful use of context, more random punctuation.)

The GPT2 model was tuned using Max Woolf's [colab](https://colab.research.google.com/drive/1VLG8e7YSEwypxU-noRNhsv5dW4NfTGce#scrollTo=aeXshJM-Cuaf) and served locally using his [gpt-2-cloud-run](https://github.com/minimaxir/gpt-2-cloud-run) directions.  (Note: It uses tensorflow 1, not 2, and you need to make sure you install the right version for your platform.)

### The Images

To spruce the output up, I added little random excerpts from a tourist map of Venice, on which I wanted to draw crazy arrows and circles, but I ran out of time for visual extras.  Also, I mixed in some random Flickr photos of Venice, to really set the mood better.   I went with Flickr over Unsplash because Unsplash was way too perfect-looking.  These Flickr pics are pretty damn fine in any case. (I'll fix those links with attribution info as alt text or extra links after the deadline.)

The code is in a crappy Jupyter notebook and I probably won't clean it up much, sorry!

## Result

You can read the raw version [here](results_raw.md).