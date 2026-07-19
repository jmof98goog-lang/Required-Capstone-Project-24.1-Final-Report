Required-Capstone-Project-24.1-Final-Report
**Word Document of same filename was uploaded with formatted text and graphics.

Problem Statement
1.	Find a more optimal solution to reading Handwritten Images than basic M/L models can deliver.
2.	Determine what AI Models will perform best on the same dataset.
   
Lessons learned from “Initial Report and Exploratory Data Analysis”
It was learned from the Exploratory Data Analysis the “SVC – Support Vector Classifier” performed best overall on Handwritten Images due to Train/Test scores and “fit times”.
Logistic Regression, KNN and even Decision Tree wasn’t that bad and may have been acceptable “as is”.  However, when hyperparameters and depth settings were modified, accuracy did not improve as “fit times” increased.
It was also learned during the course that a Neural Network would probably perform best.

Data Acquisition/Data Preprocessing/Preparation
Images are from the MNIST database to remain consistent. Although Image Resolution Conversion was necessary no data or image cleanup was performed, however image rotation was used as a pre-processor.
Pipelines were configured for all models with Training and Test Sets split to x and y datasets respectively.
All Models were run consecutively with the same pipeline method (both ML and AI) to determine optimal results.

Final Project Goal 
The goal of the Final Project is to show improvements with Neural Networks as the project moves from Machine Learning Models to what we know as “AI-Artificial Intelligence”.
Models Used
K-Nearest Neighbors (KNN), Logistic Regression, SVC (Support Vector Classifier), and Decision Tree Classifier
CNN – “Convoluted Neural Network” with Image Data Augmentation

Projects Included
•	OCR_APP(1).ipynb – Initial project using 4 regression techniques K-Nearest Neighbors (KNN), Logistic Regression, SVC (Support Vector Classifier), and Decision Tree Classifier.
Results – SVC (Support Vector Classifier) performed best.
•	train score  test score  average fit time
•	model                                                        
•	knn                    0.988170    0.969444          0.023877
•	logisticregression     0.998608    0.972222          0.054223
•	svc                    1.000000    0.980556          0.082893
•	decisiontree           1.000000    0.855556          0.035528

•	CNN Basic Neural Net for Handwritten Image Daga MNIST DATABASE.ipynb
Results – CNN (Convoluted Neural Network) Basic performed better than all other M/L models used previously. Out of 10,000 samples 9908 were read correctly resulting in a 99.08% accuracy.
Total incorrect predictions: 92
Total correct predictions: 9908
(graphic on next page shows incorrect predictions)

 
•	CNN Neural Net with Augmented Images.ipynb
Results - CNN (Convoluted Neural Network) with Augmentation resulted in severe issues with recognition accuracy. 
Two augmentation techniques were applied 
1. (Flip) and 2. (Rotate at 40 degree increments)
Accuracy on image digit before augmentation
Train - 0.9049833416938782
Test -   0.9196000099182129
Accuracy on image digit after (Flip) augmentation
Train - 0.4890666604042053
Test -   0.5507000088691711
Accuracy on image digit after (Rotate at 40 degrees augmentation)
Train - 0.8007333278656006
Test -   0.8361999988555908


Model Evaluation Conclusion:
Generally Speaking, Handwritten Recognition accuracy rates must be greater than 85% accuracy to be used in most business cases. 
This is a “rule of thumb” metric in the industry understood by most practitioners.
Some business cases require more accuracy, others require less accuracy and some require 99.9% (near perfect) accuracy to justify their use in a business context.
This is why a very careful analysis must be done to determine a proper “business case fit”. If a technology with only 75% accuracy is deployed on a project that requires 85% (or 99%) accuracy, the project can (and will) be a failure if the proper technology isn’t chosen eventually.
The projects included in this Final Deliverable do, in fact, mirror the advancements in technology historically seen over the last 20 years.
Handwritten Recognition is possible with some Machine Learning techniques and can possibly be improved to perform “as well as” modern neural networks. 
However, the cost to “configure and tune” and the amount of “fit time” required for them to “run” can be prohibitively expensive when compared to Neural Networks, especially CNN’s (Convoluted Neural Networks).
More can be done to “tune” the CNN Model for better accuracy including:
1.	Exploring more epoch settings to increase nodes run – This was done, however an epoch setting of 5 was tried before rolling back to 2 epochs which seemed ideal for this dataset.
2.	Change rotation degree from 40% to 20% or 60%. This could improve performance, however testing showed it resulted in very large “fit times” as the epochs were increased.
3.	Image Conversion issues – converting from Color, Greyscale to Bitonal is also an expensive process that results in reduction of accuracy. Scanning image data natively in bitonal as a bitmap should improve accuracy rates as image conversion does not need to be performed.


