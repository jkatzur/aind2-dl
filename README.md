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

## How to Avoid Overfitting
One of the core lessons in this first section is how to avoid overfitting (and underfitting) of models. Key takeaways on that are:
* Always split in to training + testing: this is basic and foundational, but if you aren't testing on data you didn't train with you will overfit
* Punish High Coefficients with L1 and L2 Regularization: One of the most common ways to overfit is with too high coefficients. These will look great on training data (because they will dramatically reduce error by being "more certain" in their predictions), but their mistakes will have a commensurately larger affect on test error. We use L1 regularization especially when doing feature selection (because it creates a sparse result set) and L2 regularization when training models. L2 is just quadratic vs abs.
* Dropout: to avoid having some nodes have a huge impact on our models predictions we use dropout to turn off some of the nodes from our calculations in each epoch.

## Other Common Problems to Keep in Mind
* Vanishing Gradient: this problem is caused when you are moving too slowly towards the right solution. This can happen with the sigmoid function, especially early on in the process, because its gradient will be low far out from the solution. We can gain benefit from using Relu and Tanh early on to help prevent this.
* Local Minima: Another problem we face is getting stuck at a local minima. The canonical way to do this was to use random restart. That way we'll identify all of the local minima and be able to pick the lowest. An improvement over that method is to utilize the momentum of the gradient to test further than a minima. You can imagine this like a ball rolling down a hill. If you had been rolling down very quickly, we should push forward past a small bump to see if there is more downhill to go. Each of the common optimizers in Keras have their own ways of handling this. More information here: http://ruder.io/optimizing-gradient-descent/index.html
