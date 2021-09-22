# :blue_book: Notes while reading: *Deep Learning for coders with fast &amp; PyTorch*

## Extra resources
- original notebooks [gitrepo](https://github.com/fastai/fastbook)

## Chapter 02:

The chapter introduces DL to the reader with an hand-on transfer learning scenario: take a ResNet model and adapt it to a 3-way bear classifier.

I took the same approach an created a 3-way guitar classifier :guitar: (to identify Fender Stratocaster, Fender Telecaster, Gibson RD). 
- Voila dashboard [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/finale80/fastbook/HEAD?urlpath=voila%2Frender%2Fnotebooks%2Fchapter02_guitars_classifier_inference_dashboard.ipynb)

### :pushpin: TODO:
- Rework the voila dashboard into other framework (streamlit, panel, etc.)
- Search alternatives to Git LFS for storing models

## Chapter 04:

The chapter introduces the mechanics of SGD

A couple of keys aspects in the original chapter:
- The learning rate values used are different from common literature, and are not fully argumented. To me the average reader would wonder what is their impact
- The training is done without shuffling (the parameter is not mentioned, but by default is set to false). Again, one should wonder about the impact of this

Following the chapter's flow, I developed my code and added the following:
- Extended MNIST mean classifier to all digits
- Compared MNIST binary (3-vs-7) against all digits classifier
- More experiments with SDG for a parabola (epochs and learning rate)
- More experiments with SGD for MNIST binary (3-vs-7). Specifically, more on learning rate and the effect of shuffle
- Refactored MNIST binary classifier code using OOP
- More experiments for MNIST binary (3-vs-7) with a 2-layers architecture (using a first layer with 10, 30, 50, 100, and 300)
- Added MNIST binary (3-vs-7) with a 3-layers architecture (100/10 -vs- 300/50)
- Added a 10-digits classifier


## Chapter 05:
- added demostration that sigmoid(x1-x2) = softmax(x1) for a binary classifier
- added demostration that crossentropy(x, y) = softmax(x) - y
- extended image transformation examples
- re-implemented the learning rate finder
- extended comparison on selecting the learning rate
    - run `lr_find()` to discover the learning rate (namely *single_lr*)
    - train the model head for 3 cycles using the discovered learning rate: this is our *base* model
    - *single_lr policy*: unfreeze the base model and train for 10 epochs with *single_lr*
    - *double_lr policy*: rerun `lr_find()` to discover a new learning rate (namely *double_lr*), unfreeze the base model and train for 10 epochs with the new learning rate
    - *discriminative default policy*: unfreeze the base model and train for 10 epochs with the new learning rate in range (*double_lr/100, double_lr*)
    - *discriminative policy*: unfreeze the base model and train for 10 epochs with the new learning rate in range (1e-6, 1e-4) which was manually selected
