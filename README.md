<h1 align="center">✍️ Handwritten Digit Recognition using CNN</h1>

<h3>🧩 Problem Statement</h3>
<blockquote>
Handwritten digit recognition remains one of the foundational problems in computer vision and deep learning. This project aims to develop a robust deep learning model using Convolutional Neural Networks (CNNs) to accurately identify digits ranging from 0 to 9 from the MNIST dataset—a well-known benchmark in the AI community.
</blockquote>

<h3>💡 Project Description</h3>
<blockquote>
The MNIST dataset (Modified National Institute of Standards and Technology) contains <strong>70,000 grayscale images</strong> of handwritten digits (60,000 for training and 10,000 for testing), each of size <strong>28x28 pixels</strong>. Each image is labeled with a digit between 0 and 9.

We leverage CNN architecture to recognize and classify these digits with high accuracy. Our solution includes both the backend training logic and a simple GUI for live digit drawing and prediction.
</blockquote>

<h3>📦 Dataset Details</h3>
<blockquote>
<ul>
  <li><strong>Source:</strong> tensorflow.keras.datasets.mnist</li>
  <li><strong>Image Dimensions:</strong> 28x28 grayscale</li>
  <li><strong>Color Space:</strong> Black & White</li>
  <li><strong>Classes:</strong> 10 (Digits 0 to 9)</li>
</ul>
<pre>
from tensorflow.keras.datasets import mnist
(x_train, y_train), (x_test, y_test) = mnist.load_data()
</pre>
</blockquote>

<h3>🛠️ Technical Stack</h3>
<blockquote>
<ul>
  <li><strong>Language:</strong> Python</li>
  <li><strong>Frameworks:</strong> TensorFlow, Keras</li>
  <li><strong>Libraries:</strong> NumPy, Matplotlib, Pillow</li>
  <li><strong>Interface:</strong> Tkinter for GUI</li>
</ul>
</blockquote>

<h3>⚙️ Steps Followed</h3>
<blockquote>
<ol>
  <li>📥 <strong>Data Loading</strong>: Loaded MNIST dataset directly using Keras</li>
  <li>🧼 <strong>Preprocessing</strong>:
    <ul>
      <li>Normalized pixel values (0–255 → 0–1)</li>
      <li>Reshaped input to fit CNN: (60000, 28, 28, 1)</li>
    </ul>
  </li>
  <li>🏗️ <strong>CNN Architecture</strong>:
    <ul>
      <li>Conv2D → ReLU → MaxPooling → Dropout → Flatten → Dense → Softmax</li>
    </ul>
  </li>
  <li>🧠 <strong>Training</strong>: 10 epochs using Adadelta optimizer and sparse categorical cross-entropy loss</li>
  <li>📊 <strong>Evaluation</strong>: 
    <ul>
      <li>Accuracy vs. Validation Accuracy</li>
      <li>Loss vs. Validation Loss</li>
    </ul>
  </li>
  <li>🖌️ <strong>Prediction GUI</strong>:
    <ul>
      <li>Tkinter canvas for drawing digits</li>
      <li>Button to predict the digit using the trained model</li>
    </ul>
  </li>
  <li>📉 <strong>Results:</strong> Confusion Matrix and Classification Report</li>
</ol>
</blockquote>

<h3>📈 Results</h3>
<blockquote>
<ul>
  <li>✅ Achieved accuracy close to <strong>99%</strong> on test data</li>
  <li>📉 Low error rate on visually distinct digits</li>
  <li>⚠️ Some misclassifications observed between similar digits: (1,7), (3,5), (6,9), etc.</li>
</ul>
</blockquote>

<h3>🚀 How to Run</h3>
<blockquote>
1. Clone the repository  
2. Install dependencies using:
<pre>pip install numpy tensorflow keras pillow</pre>  
3. Run the notebook to train the model and save it as `mnist.h5`  
4. Launch the GUI (`tkinter_app.py`) to draw and predict digits
</blockquote>

<h3>🎯 Project Goals</h3>
<blockquote>
<ul>
  <li>To accurately recognize handwritten digits using CNN</li>
  <li>To build a lightweight GUI for real-time digit prediction</li>
  <li>To demonstrate practical image classification with deep learning</li>
</ul>
</blockquote>

<h3>🔗 Credits</h3>
<blockquote>
Developed by <strong>C. Vishal Goud</strong> as part of the Artificial Intelligence Minor Project, November Batch  
Dataset: <strong>MNIST - Yann LeCun, Corinna Cortes, and Christopher J.C. Burges</strong>
</blockquote>
