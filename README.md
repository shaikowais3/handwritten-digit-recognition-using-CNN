Handwritten Digit Recognition Using CNN 📌 Project Overview

This project implements a Handwritten Digit Recognition System using a Convolutional Neural Network (CNN) built with TensorFlow and Keras.

The model is trained on the MNIST dataset, which contains grayscale images of handwritten digits (0–9). It can recognize handwritten digits from uploaded images or drawings using an interactive web interface powered by Gradio.

🚀 Features Recognizes handwritten digits from 0 to 9. Uses a CNN for image classification. Trains on the MNIST dataset. Displays sample training images. Shows training and validation accuracy. Evaluates model performance on test data. Predicts digits from individual test images. Saves the trained model in .keras format. Provides an interactive Gradio web interface. Supports both image uploading and drawing digits. 🛠️ Technologies Used Python – Programming language TensorFlow / Keras – Deep learning framework NumPy – Numerical operations Matplotlib – Data visualization Gradio – Interactive web interface Pillow (PIL) – Image processing MNIST Dataset – Handwritten digit dataset 📂 Project Structure text Handwritten-Digit-Recognition/ │ ├── handwritten_digit_recognition.ipynb ├── handwritten_digit_model.keras ├── README.md └── requirements.txt

📦 Installation

Install the required Python libraries:

bash pip install tensorflow numpy matplotlib gradio pillow

Alternatively, create a requirements.txt file:

text tensorflow numpy matplotlib gradio pillow

Install dependencies using:

bash pip install -r requirements.txt

▶️ How to Run Clone this repository: bash git clone https://github.com/your-username/Handwritten-Digit-Recognition.git

Navigate to the project directory: bash cd Handwritten-Digit-Recognition

Install the required dependencies: bash pip install -r requirements.txt

Open the Jupyter Notebook or Google Colab. Run all the code cells (the complete implementation can also be placed in one cell). The program will: Load the MNIST dataset. Preprocess the images. Build the CNN model. Train the model for 5 epochs. Evaluate model accuracy. Display training accuracy graphs. Save the trained model. Launch the Gradio web application. 🧠 CNN Model Architecture

The CNN model consists of the following layers:

Layer Configuration Input 28 × 28 × 1 Conv2D 32 filters, 3 × 3, ReLU MaxPooling2D 2 × 2 Conv2D 64 filters, 3 × 3, ReLU MaxPooling2D 2 × 2 Flatten Converts feature maps into a vector Dense 128 neurons, ReLU Dropout 0.3 Output 10 neurons, Softmax

Optimizer: Adam

Loss Function: Sparse Categorical Crossentropy

Evaluation Metric: Accuracy

Training Epochs: 5

Batch Size: 128

📊 Dataset

This project uses the MNIST dataset.

Training images: 60,000 Testing images: 10,000 Image dimensions: 28 × 28 pixels Color format: Grayscale Number of classes: 10 (digits 0–9)

The pixel values are normalized between 0 and 1 before training.

🌐 Web Application

The Gradio interface provides two modes:

Upload Image
Upload an image containing a handwritten digit. The model predicts the digit and displays the top three prediction probabilities.

Draw Digit
Draw a handwritten digit (0–9) directly on the drawing canvas. The model predicts the digit.

The application is launched using:

python demo.launch(share=True)

This generates a shareable Gradio link when the application is running.

💾 Model Saving

The trained CNN model is saved as:

text handwritten_digit_model.keras

You can load the saved model later using:

python model = tf.keras.models.load_model("handwritten_digit_model.keras")

🎯 Expected Output

The project produces:

Sample MNIST handwritten digit images. CNN model architecture summary. Training and validation accuracy. Test loss and test accuracy. Predicted digit with actual label. Saved trained model. Interactive Gradio web application. 🔮 Future Improvements Improve prediction accuracy with hyperparameter tuning. Add image preprocessing for better recognition. Support multiple handwritten digits in one image. Deploy the application online. Improve recognition of different handwriting styles. 👨‍💻 Author

T.Janice Abraham & Shaik Owais

📄 License

This project is intended for educational and learning purposes. You are free to modify and improve the implementation.
