Why LSTMs (or GRUs)
====================
Consider these two sentences:

1. The lucky woman went to the awards with her friends.
2. The lucky woman, having won a free ticket from the fan club, went to the wards.

Convnets (CONV1D) and simple Recurrent Neural Networks (RNN) can easily learn the relationship between "woman" and "went" in the first sentence 
since they are just one time-step or token apart. However, using CONV1D or RNN with the second sentence, it will be impossible to learn the relationship 
between "woman" and the main verb "went" because these are more than one time-step apart. We’ve lost the connection (semantic connection) between the 
subject (woman) and verb (went) of the sentence.

Long Short-Term Memory (LSTM) is designed to remember the core thought across the entire input sequence. LSTMs does this by introducing the concept of 
state for each layer in the RNN. These states act as memories. The rules that govern the information stored in the state (or memory or LSTM cells) are 
trained neural nets (weights) themselves — trained during the training of the model!

LSTM models can be trained to learn what to remember, while at the same time the rest of the RNN net learns to predict the target label! With the 
introduction of a memory and state, the model can learn dependencies that stretch not just one or two tokens away, but across the entirety of each data 
sample.

The modern version of LSTM is known as Gated Recurrent Unit (GRU), developed by Chung et al. in 2014. GRU layers work using the same principle as LSTM 
(but with a bit less representational power compared to LSTM). They’re somewhat lightweight and thus computationally cheaper to train (especially in
 training sequence-to-sequence networks). 
This trade-off between computational expensiveness and representational power is worth it (Backpropagation Through Time - BPTT is an extremely expensive 
computation!).


I made use of knowledge from the following sources:

Natural Language Processing in Action by Hobson Lane, Cole Howard and Hannes Max Hapke
Deep Learning with Python by Francois Chollet

The dataset is maintained by Maas, Andrew L.  and  Daly, Raymond E.  and  Pham, Peter T.  and  Huang, Dan  and  Ng, Andrew Y.  and  Potts, Christopher
Proceedings of the 49th Annual Meeting of the Association for Computational Linguistics: Human Language Technologies


I'm looking for a job!
cyprofusi@hotmail.com