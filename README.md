# venice_directions_nanogenmo

V2, improved version of my nanogenmo 2019 entry, "Directions in Venice." 

This project uses data from OpenStreetMap for places in Venice, Tracery grammar to generate static directions and prompts for the GPT-2 model, a GPT-2 model trained on Venice historical open source books and purchased guidebooks, and the model uses recent context plus atmosphere priming for the output.  There are random images pulled from flickr pics of Venice (hopefully :) and segments of a tourist map of Venice, on which scribbled annotations have been randomly added.

The improvements since Nanogenmo came from a longer training time on the model, for slightly better output grammar and sense; plus some improved output cleaning and prompt code.  Also added attribution links to the flickr images and scary hand-drawn annotations on the map excerpts.

### Background Story

When I was in Venice in mid-November, my AirBnB host tried to give me directions to some places he liked using a paper map.  Every time he circled a square and paused, I thought, "This is where it is," and it wasn't.  The directions kept going on and on and were really complicated because Venice is complicated (or was, without mobile GPS).  I wanted to recreate the experience of listening to him.

He also interspersed historical and suggested detours in his directions, which is the bulk of the experience here.  Plus some details from what I saw in Venice in the frame story.

### Some Tech Details

This project used Tracery grammars ([pytracery](https://github.com/aparrish/pytracery) from Allison Parrish), downloaded data on canals and roads from Open Street Map (wow that was non-obvious), plus a small GPT-2 model I ran locally, trained on historic and recent guidebooks/ histories of Venice (Gutenberg books plus a couple I purchased).

The GPT-2 model was tuned using Max Woolf's [colab](https://colab.research.google.com/drive/1VLG8e7YSEwypxU-noRNhsv5dW4NfTGce#scrollTo=aeXshJM-Cuaf) and served locally using his [gpt-2-cloud-run](https://github.com/minimaxir/gpt-2-cloud-run) directions.  (Note: It uses tensorflow 1, not 2, and you need to make sure you install the right version for your platform.)

The "mood" of the generated text is supposed to change over the course of the story, using a progress percentage calculator to determine certain prompt texts to feed to the model.  The end sections are darker, colder, and creepier, theoretically!  Venice at night is sometimes quite gothic. However, not all generated text uses the mood alteration, and so it's not consistent in tone alteration.


### The Images

To spruce the output up, I added little random excerpts from a tourist map of Venice, on which I added crazy annotations.  Also, I mixed in some random Flickr photos of Venice, to really set the mood better.  It may be that not all the images are actually Venice, depending on how the random selection with keywords went. Btw, I went with Flickr over Unsplash because Unsplash was way too perfect-looking.  These Flickr pics are pretty damn fine in any case. 

The slightly improved code is in the V2 Jupyter notebook.

## Result

You can read the latest raw version [here](raw7/results_raw7.md).