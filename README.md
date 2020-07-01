# This Chinese character does not exist

This program uses a Generative Adverserial Neural Network (GANN) to create glyphs that appear to be Chinese characters, but are in fact completely undecipherable. The basic idea is similar to that of fake faces: **we consider Chinese characters to be a sample from a distribution, and train our network to learn this distribution**.

Some fake characters generated by our network:

![Generated characters](https://i.imgur.com/Xi27EsW.png) 

Note that this is a qualitatively different task from handwriting existing characters: we are not thinking of a character as a cluster or distribution of its own (and each data point to be an "instance" or style of this), but rather we are considering *each character to be its own data point*. This is also the reason why I chose Chinese characters for this task -- there are over 80,000 unique Chinese characters (which I downloaded from [this webpage](http://hanzidb.org/character-list?page=749)). On the other hand, English would only allow us a sample of size 26 (of course, it should still be possible for an AI to make fake English letters -- humans can do it -- and would involve some form of transfer learning or neural style transfer).

## Guide to files
* `fake_characters.ipynb` is the notebook you want to play with.
* `Generator` and `Discriminator` are the saved Keras models which we use in `fake_characters.ipynb`.
* Ignore `dumps`.
* The original training script is available at this [Colab Notebook](https://colab.research.google.com/drive/1nM-fUdI9O_Ot5a8PUsu3dm0Vq2Pqhn0-?usp=sharing), and takes about 10 hours to run.
