# Handwritten-Digit-Recognition-MNIST-

1. Reason Behind Choosing This Project:
The primary reason I chose this project is to bridge my foundational knowledge of machine learning into Deep Learning and Computer Vision. The MNIST dataset is the benchmark standard for image classification. Building a CNN model helped me understand how computers process images, extract spatial features, and perform multi-class classification using neural networks.

2. How It Helps the Business:
Automated Document Processing: In banking, insurance, and postal services, millions of paper documents, checks, and application forms contain handwritten numbers. This technology automates reading them, saving thousands of manual hours.

Optical Character Recognition (OCR): It forms the foundational core for advanced OCR systems used to digitize historical records, invoices, and legal paperwork.

Error Reduction & Speed: Automating data extraction from handwritten forms drastically reduces human data-entry errors and speeds up processing pipelines.

3. Step-by-Step Technical Execution:
Step 1: Dataset Loading & Understanding

I used the benchmark MNIST dataset built directly into TensorFlow/Keras, which contains 60,000 training images and 10,000 testing images of handwritten digits (0 through 9).

Step 2: Data Preprocessing & Normalization

Since pixel values range from 0 to 255, I normalized the image data by dividing by 255.0 to scale values between 0 and 1, helping the neural network converge faster during training.

I reshaped the image dimensions into a 4D tensor (28x28x1) to make it compatible with the Convolutional Neural Network architecture.

Step 3: CNN Model Architecture Design

I built a sequential Deep Learning model using TensorFlow and Keras:

Conv2D Layers: Used 32 and 64 filters with ReLU activation to automatically extract spatial features like edges, curves, and loops from the digits.

MaxPooling2D Layers: Added pooling layers to downsample the image representation and reduce computational complexity.

Flatten & Dense Layers: Flattened the 2D feature maps into a 1D vector and passed them through fully connected dense layers with ReLU.

Output Layer: Used a Dense layer with 10 nodes and Softmax activation to output probability distributions across the 10 digits (0–9).

Step 4: Model Compilation & Training

I compiled the model using the Adam optimizer and sparse categorical crossentropy loss function (since it's a multi-class classification problem).

I trained the model using model.fit() over a few epochs on the training data.

Step 5: Model Evaluation & Results

Finally, I evaluated the trained model on unseen test images and achieved an exceptional test accuracy of over 98.5%.
