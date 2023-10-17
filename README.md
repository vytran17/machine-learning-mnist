# Deep Learning Recognizer of Handwritten Digits

Run `run_mnist.py` to train and evaluate the deep learning network on a standard MNIST dataset.

Comment out to test different sets of hyperparameters.

Use network2 and network3 if needed for different architecture.

Implementation is based on https://github.com/MichalDanielDobrzanski/DeepLearningPython

Analysis of running the network with 3 sets of hyperparameters:

- Hyperparameter #1 had 30 neurons, 3.0 learning rate. It took 2min and went from 82% to 95% in 30 epoch
- Hyperparameter #2 had 100 neurons in the hidden layer. It was slower than #1 as expected (more neurons, more weights, more time to train). 2min8sec vs 3min56sec
- Hyperparameter #2 was run twice. The first time it went from 56% to 78% (not good but only because initial random weights were bad). The second time it went from 83% to 96%. So it got even better than Hyperparameter #1. Because more neurons, better fit. And first run was bad because it had a bad random start.
- Hyperparameter #3 was the same 100 neurons but 0.01 learning rate instead of 3.0. It took 3m74 and accuracy went from 11% to 12%. Really bad accuracy because the learning rate is too low, and barely improved in 30 epochs.
- So we learned that hyperparameter #2 is so far the best even though slower than #1.
