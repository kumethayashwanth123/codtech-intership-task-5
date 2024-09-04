# codtech-intership-task-5
**Name:** KUMETHA YASHWANTH

_**Company:**_ CODTECH IT SOLUTIONS

**ID:** CT6WDS1401

**Domain:** ARTIFICAL INTELLIGENCE

**Duration:**  from JULY 20th, 2024 to SEPTEMBER 5th, 2024.

**Mentor:** MUZAMMIL AHMED

**Overview of the Code**

This code implements a Generative Adversarial Network (GAN) using TensorFlow and Keras to generate images similar to those in the MNIST dataset, which consists of handwritten digits.

**Key Components:**

**Data Preprocessing:**


The MNIST dataset is loaded and preprocessed. The images are reshaped to include a channel dimension (28x28x1) and normalized to a range of [-1, 1] to match the output of the generator.

**Dataset Creation:**

A TensorFlow dataset is created from the training images, shuffled, and batched. This prepares the data for feeding into the GAN during training.

**Generator Model:**

The generator is a neural network that takes a random noise vector (100 dimensions) as input and generates a 28x28x1 image.
The architecture consists of dense layers, followed by reshaping, transposed convolutions (Conv2DTranspose), batch normalization, and Leaky ReLU activation functions. The final layer uses a tanh activation function to ensure the output is within the range [-1, 1].

**Discriminator Model:**

The discriminator is a neural network that takes an image as input and outputs a single scalar value, representing whether the input image is real (from the dataset) or fake (generated).
The architecture includes convolutional layers with strides, followed by Leaky ReLU activations, dropout layers, and a dense output layer.

**Loss Functions:**

The GAN uses Binary Cross-Entropy loss. The discriminator's loss combines the losses from both real and fake images, while the generator's loss is based on how well it can fool the discriminator.

**Optimizers:**

Both the generator and discriminator are optimized using the Adam optimizer with a learning rate of 1e-4.

**Training Step:**

During each training step, random noise is generated and passed through the generator to create fake images.
Both real and fake images are passed through the discriminator.
The losses for both models are computed, and gradients are calculated and applied to update the model weights.

**Training Loop:**

The GAN is trained over a specified number of epochs. After each epoch, the generator produces a set of images, which are saved and displayed.
The train function controls the overall training process, calling the train_step function for each batch of images.

**Image Generation:**

After each epoch, a function generate_and_save_images is used to create and save images produced by the generator, allowing you to visualize the progress of the GAN.

**Conclusion**

This code successfully implements a simple GAN to generate images resembling those in the MNIST dataset. The generator learns to create realistic images of handwritten digits, while the discriminator learns to distinguish between real and fake images. Over multiple epochs, the generator improves its ability to produce realistic images, and the discriminator becomes more accurate in identifying fakes. The saved images after each epoch provide a visual confirmation of the GAN's learning process, showing how the generated images evolve and improve over time.

GANs are powerful tools in deep learning, and this code provides a foundational example of how to build and train one using TensorFlow. The final results depend on factors like the number of training epochs, batch size, and hyperparameters, and further tuning can lead to even better image generation performance.
**OUTPUT**
![WhatsApp Image 2024-09-04 at 18 57 32_32ed2c1d](https://github.com/user-attachments/assets/942ccd35-cac4-431a-88a3-0b72f976cb22)
![WhatsApp Image 2024-09-04 at 18 57 55_66a273c2](https://github.com/user-attachments/assets/838998a6-89b0-416e-9a5f-45678ee383e8)
![WhatsApp Image 2024-09-04 at 18 58 07_1639b931](https://github.com/user-attachments/assets/4aed0373-9d3d-434d-8b8c-7a7ef41cc23a)
![WhatsApp Image 2024-09-04 at 18 58 18_49d54ccf](https://github.com/user-attachments/assets/00743708-beed-4e03-b28c-b840d4aeeef0)


