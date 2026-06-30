# Short intro about project

# NanoGPT — Transformer Language Model Built from Scratch

A from-scratch PyTorch implementation of a character-level GPT language model, progressing from a baseline bigram 
model to a full 6-layer, 6-head transformer with 384-dimensional embeddings (~10.7M parameters). Built to deeply 
understand transformer internals — every core component (scaled dot-product self-attention, multi-head attention, 
causal masking, position-wise feedforward layers) is implemented manually rather than relying on pre-built libraries.

Trained on a 1M+ character Shakespeare corpus with a 90/10 train-validation split, using AdamW optimization and 
dropout regularization to monitor convergence over 5,000 training iterations.

> Implementation follows Andrej Karpathy's "Neural Networks: Zero to Hero" lecture series — built as a deep dive 
> into first-principles transformer architecture and attention mechanisms.

**Tech stack:** PyTorch · Python


Brief Description about the Project

# nanogpt-lecture

Code created in the [Neural Networks: Zero To Hero](https://karpathy.ai/zero-to-hero.html) video lecture series, specifically on the first lecture on nanoGPT. Publishing here as a Github repo so people can easily hack it, walk through the `git log` history of it, etc.

NOTE: sadly I did not go too much into model initialization in the video lecture, but it is quite important for good performance. The current code will train and work fine, but its convergence is slower because it starts off in a not great spot in the weight space. Please see [nanoGPT model.py](https://github.com/karpathy/nanoGPT/blob/master/model.py) for `# init all weights` comment, and especially how it calls the `_init_weights` function. Even more sadly, the code in this repo is a bit different in how it names and stores the various modules, so it's not possible to directly copy paste this code here. My current plan is to publish a supplementary video lecture and cover these parts, then I will also push the exact code changes to this repo. For now I'm keeping it as is so it is almost exactly what we actually covered in the video.

### License

MIT
