# :blue_book: Notes while reading: *Deep Learning for coders with fast &amp; PyTorch*

## Extra resources
- original notebooks [gitrepo](https://github.com/fastai/fastbook)

## Chapter 02:

Create a  ResNet-based image classifier to detect 3 types of guitars: Fender Stratocaster, Fender Telecaster, Gibson RD. 
- voila dashbard [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/finale80/fastbook/HEAD?urlpath=voila%2Frender%2Fnotebooks%2Fchapter02_guitars_classifier_inference_dashboard.ipynb)

## Chapter 04:

I followed the original flow of the chapter, but using my own code for the most part and added the following:
- extended MNIST mean classifier to all digits
- compared MNIST binary (3-vs-7) against all digits classifier
- more experiments with SDG for parabol (epochs and learning rate)
- more experiments with SGD for MNIST binary (3-vs-7). Specifically, more on learning rate and the effect of shuffle

### TODO:
- extend the code so to support a 10-digit classifier

