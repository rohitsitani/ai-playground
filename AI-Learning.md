Tansformer architecture

https://www.youtube.com/watch?v=RDvQmE9eNRw&list=PLTB9HGiKZPe8VONYxDxvoID910Dd307UV
1. install docker 
1.1 brew install --cask docker
1.2 brew install docker
2. install ollama
3. setup open webUI - 
3.1 docker pull ghcr.io/open-webui/open-webui:main
3.2 https://github.com/open-webui/open-webui?tab=readme-ov-file#installation-with-default-configuration
4. install deepseek

A. Model size / Model Parameters - more parameters, more complex to train and deploy. Parameters are values learned by the model during training. They are often part of the model’s architecture and help make predictions based on the input data
A.1. Weights and Biases: These are adjusted during training to minimize the error between the predicted output and the actual label.
A.2. Number of Layers: Determines the depth of the model (e.g., how many stacked layers of neural networks).
Example: GPT-3 has 96 layers.

B. Training data - quality and quantity impacts performance. LLM parameters are set to an initial value based on previous training or by randomness. The model is fed with large amounts of textual data. During training, the model takes the input and predicts the correct output. Then, it compares the predicted output to the actual text to check the accuracy of its prediction. The model iteratively learns from its mistakes and adjusts its parameters accordingly. With each adjustment, the model increases its prediction accuracy.  
https://www.alexanderthamm.com/en/blog/the-role-of-parameters-in-llms/

C. Decoding Hyperparameters
1.Temperature - creativity
2. Token numbers -  length of the response
3. Top-k and Top-p Sampling: Adjusts randomness in output.
Top-k Sampling: Selects the next word from the top-k most probable tokens.
Top-p Sampling (Nucleus Sampling): Chooses from tokens that form the top-p cumulative probability.
Top-p - number of words that are considered candidates for the next word during the text-generation process
4. Presence penalty - output reflects the presence of certain words or phrases for repetition
5. frequency Penalty - number of times the token appears in the text, including in the prompt
6. Decoding Type (Greedy vs. Beam Search): Controls how the model selects the next word/token.
Greedy Search: Picks the word with the highest probability at each step.
Beam Search: Explores multiple possible sequences and picks the most likely overall sequence.

https://medium.com/@santoshpandey987/llm-parameters-and-hyperparameters-explained-2ba876dbae29

D. Training Hyperparameters
1. Number of Layers/Units: Refers to the number of layers or units in each layer of the neural network. Example: More layers can lead to better learning capacity, but too many can overfit the model.
2. Dropout Rate: Prevents overfitting by randomly “dropping out” neurons during training. Example: A dropout rate of 0.2 means 20% of the neurons are ignored in each forward pass.
3. Batch Size: Controls the number of samples fed into the model at one time. Smaller batches allow for more frequent updates, while larger batches lead to smoother gradient calculations. Example: A batch size of 32 or 64 is common for NLP models.
4. Learning Rate: Determines how quickly or slowly the model updates its parameters during training. Too high a learning rate might overshoot the optimal solution, while too low might take too long to converge.
5. Epochs: Refers to how many times the entire dataset is passed through the network during training. More epochs allow for better learning, but too many can overfit the model.

E. Optimization Hyperparameters
1. Early Stopping: Stops training when performance ceases to improve, avoiding overfitting.
2. Learning Rate Scheduling: Dynamically adjusts the learning rate based on training progress. Example: Reduce learning rate when performance stagnates, ensuring smaller, finer updates toward the end of training.
3. Gradient Clipping: Prevents large updates by limiting the size of the gradients, which can be especially important in RNNs.
4. Regularization: Adds a penalty to the loss function for more complex models, encouraging simpler models that generalize better.

F. Evaluation Hyperparameters
Validation and Evaluation: After training, evaluating the model with a holdout dataset is key for understanding generalization performance. Metrics like accuracy, precision, recall, and perplexity can be calculated.

new models does not just rely on parameters but has better algorithms to improve/learn abilities at lower parameter value.

The data quality, computational resources, and the application's specific requirements define the model's success

Companies are demanding their teams to train efficient models that solve customer's needs and create models trained for specific applications

https://www.thecloudgirl.dev/blog/llm-parameters-explained
Gemini Nano has 1.8 billion parameters. What does it mean? Compared to larger AI models, 1.8 billion is a relatively small number of parameters.

This indicates that Gemini Nano is designed for efficiency and running on devices with limited resources, like smartphones.

Despite its smaller size, it still shows good performance in tasks like summarizing text and suggesting replies in chat applications, thanks to its efficient architecture and training.