# Badly Drawn Boys
Back in november 2016, Google convinced 100,000s of people to draw bad pictures of 345 distinct categories of thing (dog, cat, boat etc.) with an experiment called [Quickdraw](https://quickdraw.withgoogle.com/). They've also opensourced a lot of the resulting data.

People have used the data to train neural networks to answer the question 'is this a drawing of a dog or a cat?'. That's a super easy task these days - It took me about an hour to write a script to do the job with around 85% accuracy. That's not awful, given the tiny data we're working with and the massive amount of similarity between classes. I'd be surprised if human performance was significantly better on cats and dogs. Training the same model with different class choices (still from quickdraw) we can easily bump that up to >99% accuracy. You can see the classifier work [here](notebooks/classifier.ipynb).  
This kind of classification job is a standard toy ML problem. MNIST is the almost always first dataset you hear about in any ML/neural network tutorial or course, and the quickdraw data has been deliberately assembled to look and behave like MNIST.  
I'd like to dig a bit deeper.

I want to see what the space _between_ dog drawings looks like. For example, are there classes of dog drawings that we can infer automatically by just looking at unlabelled drawings of that one class? If we _can_ cluster types of dogs, can we then map that space and represent the differences between them somehow?

In other, more mathematically precise words, I want to explore the latent space of these drawings.
