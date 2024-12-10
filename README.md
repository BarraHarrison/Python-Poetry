## Poetic Text Generation with Recurrent Neural Networks in Python





This project explores recurrent neural networks (RNNs), specifically using a Long Short-Term Memory (LSTM) layer in Python,
to generate poetic text based on Shakespeare's works.
The aim is to gain practical experience with text generation and understand the capabilities of RNNs in modeling sequential data.

## How the Code Works

Data Preparation:
The Shakespeare text is downloaded and preprocessed by:
Converting it to lowercase.
Trimming the text to a manageable subset.
Characters are mapped to indices and vice versa to enable numerical processing.

Sequence Creation:
The text is divided into sequences of fixed length (SEQ_LENGTH) with a sliding
window approach (STEP_SIZE), creating input (sentences) and output (next_characters) pairs.

One-Hot Encoding:
Input and output data are transformed into one-hot encoded representations to be compatible with the LSTM layer.

Model Architecture:
A sequential model is built with:
An LSTM layer for learning temporal patterns.
A Dense layer with a softmax activation to predict the probability distribution over the next character.

Training:
The model is trained for 4 epochs with a batch size of 256, using the categorical
cross-entropy loss function and the RMSprop optimizer. The training process minimizes
the loss to improve text prediction accuracy.

Text Generation:
A custom sampling function introduces randomness to text generation,
balancing creativity and coherence using a temperature parameter.
The generate_text function uses the trained model to generate new text,
seeded from a random starting sequence.

## What are Epochs and why do we use them in this program?

An epoch refers to one complete pass through the entire training dataset by the model.
In this project, 4 epochs were used to allow the model to iteratively learn patterns from the data.
During each epoch, the model adjusts its weights to minimize the loss function,
improving its ability to predict the next character in the sequence.
Multiple epochs were chosen to ensure the model refines its understanding,
but more epochs could further enhance its learning.




