**Text Classification with Switch Transformer**
===============================================

**Overview**
------------
This project demonstrates the implementation of the Switch Transformer model for text classification using the IMDb movie reviews dataset. The Switch Transformer is an efficient and scalable variant of the Transformer architecture that leverages a Mixture of Experts (MoE) approach to enhance model capacity without significantly increasing computational requirements.

**Implementation Details**
--------------------------
* Data Preparation: The project utilizes the IMDb movie reviews dataset for binary sentiment classification. The dataset is preprocessed to pad sequences and limit vocabulary size.
* Model Architecture: The model comprises an embedding layer, a Switch Transformer layer with multiple experts, and a classification head. The Switch Transformer layer dynamically routes tokens to different experts based on the router's decisions.
* Training: The model is trained using the Adam optimizer and sparse categorical cross-entropy loss. The training process is tracked using validation accuracy and loss metrics.

**Key Features**
----------------
* Switch Transformer Layer: Implements a Mixture of Experts routing mechanism, allowing different parts of the input to be processed by different experts.
* Load-Balanced Loss: Incorporates an auxiliary loss to ensure balanced load distribution among experts, preventing any single expert from becoming a bottleneck.
* Data Augmentation: Techniques such as random noise addition and dropout are used to enhance the generalization ability of the model and prevent overfitting.
* Regularization: Dropout and early stopping are applied to mitigate overfitting and improve model robustness.

**Results**
-----------
After training, the model's performance on the validation set is as follows:
* Training Accuracy: 93.31%
* Validation Accuracy: 86.85%

**References**
--------------
* Switch Transformer: Scaling to Trillion Parameter Models with Simple and Efficient Sparsity
* Keras Documentation
* IMDb Movie Reviews Dataset

**Contributions**
-----------------
Contributions to this repository are welcome. If you have any ideas for additional pruning experiments or improvements to the existing code, please open an issue or submit a pull request.
