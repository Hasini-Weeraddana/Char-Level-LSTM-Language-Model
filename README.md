# Char-Level-LSTM-Language-Model
### Use Case
This project demonstrates a character-level language model trained on Nietzsche's writings using an LSTM neural network. The model learns character sequences and generates new text that mimics the style and vocabulary of the input corpus. It serves as a foundational example for natural language generation (NLG) and can be extended for:
* Creative writing assistance
* Chatbot base models
* Poetic or philosophical text synthesis
* Educational demos for sequence modeling and RNNs
### Techniques Used
| Area | Technique |
| --- | --- |
| Data Source | Nietzsche's writings (from Keras dataset) |
| Preprocessing | Character-level tokenization, sequence windowing with step size |
| Model Architecture | LSTM (128 units) followed by a dense softmax layer |
| Encoding | One-hot encoding for input characters |
| Training | 20 epochs with categorical cross-entropy loss and Adam optimizer | 
| Text Generation | Temperature sampling for varying creativity and randomness |
| Framework | TensorFlow/Keras in a Jupyter Notebook environment |
### Challenges Faced
1. Training Time
   Training on ~200k character sequences using LSTM is computationally intensive. The notebook took several minutes per epoch, especially without GPU acceleration.
2. Overfitting Risk
   As the dataset is limited in diversity (one author/style), the model tends to overfit and repeat similar patterns, especially at lower temperatures.
3. Balancing Temperature
   Finding the right temperature (0.2, 0.5, 1.0) was crucial. Lower temperatures generated more fluent but repetitive text; higher temperatures led to diverse but sometimes nonsensical      outputs.
