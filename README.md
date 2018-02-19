# AIND Mini Projects

## First Mini Project -- Student Admissions
This project takes a sample data set (student_data.csv) that contains a list of
student's applying for grad school's GRE score, GPA, and class rank. We then use
Neural Nets to aim to predict which students will be admitted and which won't.
This is a simple initial assignment without doing additional variable cleaning
like removing outliers, feature scaling, feature selection, transformations (e.g PCA).
We also chose DNN up front vs playing with various algorithms.

This is a simple practice using Keras to get a feel for how it works

Go to Student_Admissions.ipynb to learn more

## Second Mini Project -- IMDB in Keras
This was a fun project to figure out if you could predict the sentiment of an IMDB
review based on the words in the review. The interesting takeaways from this project are:
* Using a Neural Net I got to .866 accuracy on test data
* Bringing in more words increased accuracy
* I expected that removing top words (e.g the, and, etc...) would improve accuracy and I was completely wrong. The model performed best with all words, including stopwords
* I was able to get better performance with fewer epochs and a smaller batch size (e.g 5 epochs and 100 batch size) than if I did 50 epochs and 1000 batches. I also tried a bunch of input along the way. 

This was another nice project to learn about how to apply Keras to models and how to optimize
