##Speaker: Jeff Dean

What is deep learning?
basically mathematical units which collaborate

Supervised learning
Unsupervised learning
Reinforcement learning

Higher layers form higher levels of abstraction

Simulate real neural systems by chemical components

Neural Networks

y =  F(sum(w_i, x_i))

What can neural nets compute?

Human perception is very fast (0.1 second)
recognize objects
recognize speech
...
only 10 sequential steps at that time

brain - massively  parallel - not many sequential steps


functions artificial neural nets can learn

input -> output
pixels : "lion"
audio: "see at tuhl res tau...."

Internal Software framework usable by anyone at Google
	- Enable both research as well as training/use of models for products
	- dozens of production...

Training model - Patience threshold

Optimize for experimental turnaround time

Train in a day what takes a single GPU card 6 weeks

Exploit parallelism
model parallelism
data parallelism

Jointly optimize things and introduce new connections

Production launching across different products.

Running neural nets on Android phones and CPUs

Broad set of problems

Writing general algorithms and throw applications at it.

Applications

Research on neural nets - parallel neural nets

Unsupervised training - 10 million YouTube videos

Take pixels, auto encoder, construct raw images of the network.

Reconstruction of other layers

60,000 neurons at that label

Half non-faces and with faces

Optimal stimulus by numerical optimization

Acoustic Modeling for Speech Recognition

30% reduction in World Error rate for English
("biggest speech recognition  in 20 years of speech research")

Convolutional Neural Net Models for Image Classification

Translation invariant!

Creating heat map to detect small texts

Deep neural network  - 1000D joint embedding space

Prediction (classification/regression)

Back propagation

Skipgram Text Model

How can be learn the embeddings?

Training on Wikipedia corpus

nearby_words, upper layes, embedding vector.


Solving Analogies

E(hotter) - E(hot) + E(big) approx. E(bigger)

Principal Components Analysis (PCA)

Sequence Prediction Model - Recurrent neural network(LSTM)

deep LSTM: multiple

Translation with Sequence Prediction

Conversation with Sequence Prediction

LSTM for End to End Translation

Linearly Separable wrt subject vs object.

High dimensional space come from sequence of tokens.

Captions with Sequence Prediction

Initial state can also come from non-sequence data.
Given a photograph, generate a caption.

Feed into LSTM

Two captions Brain suggests:

"A close up of a child holding ...."

"A baby holding...."

Deep neural networks are very effective for wide range of tasks.

Using embeddings with sparse data.

