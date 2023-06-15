# AnalisisTweetTopicModelingBert

Disaster NLP:Keras Bert using TFhub

No pooling, directly use the CLS embedding.
Since the [CLS] token is the first token in our sequence, we simply take the first slice of the 2nd dimension from our tensor of shape (batch_size, max_len, hidden_dim), which result in a tensor of shape (batch_size, hidden_dim).


No Dense layer.
Simply add a sigmoid output directly to the last layer of BERT, rather than experimenting with different intermediate layers.


Fixed learning rate, batch size, epochs, optimizer. 
The optimizer used is Adam, with a learning rate between 2e-5 and 5e-5. 
Model for 3 epochs with a batch size of 32.

Concise, reusable, and functional example of how to build a workflow around the TF2 version of BERT. 
