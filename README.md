# Continuos_Bag_of_Words


Continuous Bag of Words (CBOW) is a type of neural network model used in natural language processing (NLP) and specifically in the field of word embeddings. It is designed to predict a target word based on its context, i.e., the surrounding words in a given window. CBOW is one of the two popular architectures for training word embeddings, the other being Skip-gram.


# Architecture:

# 1.Input Layer:
The input layer of the CBOW model represents the context words within a fixed window around the target word.
Each word in the context is encoded as a one-hot vector, where the dimension of the vector is equal to the size of the vocabulary, and only the index corresponding to the word is set to 1.

# 2.Embedding Layer:
The one-hot encoded vectors are then passed through an embedding layer. This layer converts the one-hot vectors into dense word embeddings.
The embeddings are real-valued vectors with a much lower dimension compared to the one-hot vectors. The size of the embedding space is a hyperparameter and typically ranges from 50 to a few hundred dimensions.

# 3.Hidden Layer:
The embedded vectors are averaged to obtain a single vector representation of the context. This average vector serves as the input to a hidden layer.
The hidden layer performs a linear transformation on the averaged vector using a weight matrix. The output is then passed through a non-linear activation function (commonly hyperbolic tangent or rectified linear unit) to introduce non-linearity.

# 4. Output Layer:
The output layer produces a probability distribution over the vocabulary.
A softmax activation function is applied to convert the output into probabilities. Each element of the output vector represents the likelihood of a particular word being the target word. 



