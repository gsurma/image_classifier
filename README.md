<h3 align="center">
  <img src="assets/image_classifier_icon_web.png" width="300">
</h3>

# Image Classifier

Python Jupyter Notebook with **Convolutional Neural Network** image classifier implemented in **Keras**. It's **[Google Colab](https://colab.research.google.com/)** ready.

## Usage

Structure your data as follows:

	data/
		training/
		    class_a/
		        class_a01.jpg
		        class_a02.jpg
		        ...
		    class_b/
		        class_b01.jpg
		        class_b02.jpg
		        ...
		validation/
		    class_a/
		        class_a01.jpg
		        class_a02.jpg
		        ...
		    class_b/
		        class_b01.jpg
		        class_b02.jpg
		        ...

For binary classifications you are good to go!

For non-binary classifications:

* add other classes to training and validation directories
* change class_mode from "binary" to "categorical"
* change loss function from "binary\_crossentropy" to "categorical\_crossentropy"

## Performance

**Dataset:** [Dogs vs Cats](https://www.kaggle.com/c/dogs-vs-cats)

**Description:** Binary classification. Two classes two distinguish: **dogs** and **cats**.

**Training:** 10 000 images per class

**Validation:** 2 500 images per class

### Hyperparameters

	IMAGE_SIZE = 200
	IMAGE_WIDTH, IMAGE_HEIGHT = IMAGE_SIZE, IMAGE_SIZE
	EPOCHS = 50
	BATCH_SIZE = 32

### Model

	_________________________________________________________________
	Layer (type)                 Output Shape              Param #   
	=================================================================
	conv2d_7 (Conv2D)            (None, 198, 198, 32)      896       
	_________________________________________________________________
	activation_11 (Activation)   (None, 198, 198, 32)      0         
	_________________________________________________________________
	max_pooling2d_7 (MaxPooling2 (None, 99, 99, 32)        0         
	_________________________________________________________________
	conv2d_8 (Conv2D)            (None, 97, 97, 32)        9248      
	_________________________________________________________________
	activation_12 (Activation)   (None, 97, 97, 32)        0         
	_________________________________________________________________
	max_pooling2d_8 (MaxPooling2 (None, 48, 48, 32)        0         
	_________________________________________________________________
	conv2d_9 (Conv2D)            (None, 46, 46, 64)        18496     
	_________________________________________________________________
	activation_13 (Activation)   (None, 46, 46, 64)        0         
	_________________________________________________________________
	max_pooling2d_9 (MaxPooling2 (None, 23, 23, 64)        0         
	_________________________________________________________________
	flatten_3 (Flatten)          (None, 33856)             0         
	_________________________________________________________________
	dense_5 (Dense)              (None, 64)                2166848   
	_________________________________________________________________
	activation_14 (Activation)   (None, 64)                0         
	_________________________________________________________________
	dropout_3 (Dropout)          (None, 64)                0         
	_________________________________________________________________
	dense_6 (Dense)              (None, 1)                 65        
	_________________________________________________________________
	activation_15 (Activation)   (None, 1)                 0         
	=================================================================
	Total params: 2,195,553
	Trainable params: 2,195,553
	Non-trainable params: 0
	_________________________________________________________________

### Results

<img src="results/shakespeare/loss.png" width="500">

