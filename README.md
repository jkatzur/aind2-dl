# Mini Project - Student Admissions
This project takes a sample data set (student_data.csv) that contains a list of
student's applying for grad school's GRE score, GPA, and class rank. We then use
Neural Nets to aim to predict which students will be admitted and which won't.
This is a simple initial assignment without doing additional variable cleaning
like removing outliers, feature scaling, feature selection (we only have 3 though),
transformations (e.g PCA). We also chose DNN up front vs playing with various algorithms.

It's just a sample to practice using Keras and get a feel for how it works. 

Readme from course below:

### Instructions

1. Clone the repository and navigate to the downloaded folder.

	```
		git clone https://github.com/udacity/aind2-dl.git
		cd aind2-dl
	```

2. Obtain the necessary Python packages, and switch Keras backend to Tensorflow.  

	For __Mac/OSX__:
	```
		conda env create -f requirements/aind-dl-mac.yml
		source activate aind-dl
		KERAS_BACKEND=tensorflow python -c "from keras import backend"
	```

	For __Windows__:
	```
		conda env create -f requirements/aind-dl-windows.yml
		activate aind-dl
		set KERAS_BACKEND=tensorflow
		python -c "from keras import backend"
	```

	For __Linux__:
	```
		conda env create -f requirements/aind-dl-linux.yml
		source activate aind-dl
		KERAS_BACKEND=tensorflow python -c "from keras import backend"
	```

3. Enjoy!
# aind2-dl
