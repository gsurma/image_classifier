<h3 align="center">
  <img src="assets/image_classifier_icon_web.png" width="300">
</h3>

# Image Classifier

Python Jupyter Notebook with **Convolutional Neural Network** image classifier implemented in **Keras** 🖼️. It's **[Google Colab](https://colab.research.google.com/)** ready.

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
