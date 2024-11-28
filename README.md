# handwritten-digit-recognition
Simple Project For Detecting Handwritten Digits Using Tensorflow Framework.<br>

Trained on a dataset provided by MNIST DATABASE.
The data set contains ***5000*** training examples of handwritten digits
- Each training example is a ***20-pixel x 20-pixel*** grayscale image of the digit.
- Each pixel is represented by a floating-point number indicating the grayscale intensity at that location.
- The 20 by 20 grid of pixels is “unrolled” into a 400-dimensional vector.
- Each training examples becomes a single row in our data matrix **X**.
- This gives us a ***5000 x 400*** matrix **X** where every row is a training example of a handwritten digit image.

The model we are using for this project has 2 dense layers with ReLU activation and 1 output layer with Linear activation.<br>
Below is a visualisation of the described model:
![Screenshot (130)](https://github.com/user-attachments/assets/b15855a1-17a6-427a-a622-966cf3db1f0c)

Weights and Biases for each layer are:
- Layer 1: The shape of W1 is (400, 25) and the shape of b1 is (25)
- Layer 2: The shape of W2 is (25, 15) and the shape of b2 is: (15)
- Layer 3: The shape of W3 is (15, 10) and the shape of b3 is: (10)


Model Details:
| Layer (type)                      | Output Shape               | Parameters   |
| --------------------------------- | -------------------------- | ------------ |
| L1 (Dense)                        | (None, 25)                 | 10025        |
| L2 (Dense)                        | (None, 15)                 | 390          |
| L3 (Dense)                        | (None, 10)                 | 160          |

<br>We could also use an outpt layer with Softmax activation for calculating the probability of each digit.
But since we want to output the correct digit and not the probability, we use a layer with Linear ativation.
