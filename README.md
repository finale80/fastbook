# :blue_book: Notes while reading: *Deep Learning for coders with fast &amp; PyTorch*

## Extra resources
- original notebooks [gitrepo](https://github.com/fastai/fastbook)

## Chapter 02:

The chapter introduces DL to the reader with an hand-on transfer learning scenario: take a ResNet model and adapt it to a 3-way bear classifier.

I took the same approach an created a 3-way guitar classifier :guitar: (to identify Fender Stratocaster, Fender Telecaster, Gibson RD). 
- voila dashboard [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/finale80/fastbook/HEAD?urlpath=voila%2Frender%2Fnotebooks%2Fchapter02_guitars_classifier_inference_dashboard.ipynb)

### :pushpin: TODO:
- rework the voila dashboard into other framework (streamlit, panel, etc.)
- search alternatives to Git LFS for storing models

## Chapter 04:

The chapter introduces the mechanics of SGD

Following the chapter's flow, I developed my code and added the following:
- extended MNIST mean classifier to all digits
- compared MNIST binary (3-vs-7) against all digits classifier
- more experiments with SDG for a parabola (epochs and learning rate)
- more experiments with SGD for MNIST binary (3-vs-7). Specifically, more on learning rate and the effect of shuffle

### :pushpin: TODO:
- extend the code so to support a 10-digit classifier

