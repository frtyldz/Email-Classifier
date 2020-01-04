# Email-Classifier

KNN)

	-	Before running the code, you should first upload the csv files imported there inside
		genfromtxt() method.

	-	All the datas requested in the question has been coded and printed inside the code.
	
	-	You can run the code with different k values by changing k value at the top. 

	-	The code between time methods do all the calls, print accuracy, precision and time. 


Naive Bayes)

	-	Before running the code, you should first upload the csv files imported there inside
		read_csv() method.

	-	All the datas requested in the question has been coded and printed inside the code.

	- 	getVarNum() method do everything but it is ended to you with MAP implementation. If 		you want to see the MLE solution as well, MLE solution was also added to getVarNum() 		method as commented. You can remove the comment and see the output. This was 		commented because of the time consumption.

	-	Which part of the question those codes belong to was commented above the code 		parts.




3 DrugBank Drug Target Identifiers Data Set 
Biological sciences are becoming data-rich and information-intensive. Machine learning applications have become very useful and popular tools for resolving important questions in biology by enabling to analyze vast amount of biological information. In this question, you will be introduced to one of the biological data sets, DrugBank, and gain intuition of feasibility of kNN algorithm using this data set.
Data set
The data set contains their 4765 unique proteins and 136 unique drugs that target those proteins. [2] Your job is to predict whether a protein is pharmacologically active, i.e. directly related to the mechanism of action for at least one of the associated drugs, or not by using the target information of drugs.
The data has been split into training and validation subsets with the ratio of 3812/953 i.e. 20% of the proteins are taken for the validation set. You will use the following files:
• question-3-train-features.csv
2
• question-3-train-labels.csv
• question-3-valid-features.csv
• question-3-valid-labels.csv
• question-3-train-protein-index.csv • question-3-valid-protein-index.csv • question-3-drug-index.csv
The files that end with features.csv contain the features and the files ending with labels.csv contain the ground truth labels.
In the feature files, each row contains the feature vector for a protein. The j-th term in a row i, is the target information of the j-th drug for the i-th protein. The label files include the ground truth label for the corresponding proteins where the order of the proteins (rows) are the same as the features file. That is the i-th row in the files corresponds to the same protein. Any protein is labeled as either active (1) or inactive (0).
The files ending with index.csv are the index files in which the first element in j-th is the protein or drug that j-th row or column represents in the feature files.
Question 3.1 [5 pts] Take a quick look to your feature files and decide on a distance metric for your kNN classifier. Briefly explain your motivation for choosing your distance metric. What would happen if you used another metric to calculate distances?
Question 3.2 [12 pts] Train your kNN classifier ∀ k ∈ [1, 3, 5, 10, 20, 50, 100, 200]. You do not have to use all values if you observe a trend in the outputs. Report accuracy and precision on validation set for each of your training sessions. You may use plots or tables. Comment on your results. What have you expected and are the result parallel or contradictory to your expectations?
In addition, make note of training time and validation time of your classifier for the next question.
Question 3.3 [8 pts] Comment on the run times that you have noted in the previous question. You may use plots or tables to support your comments. Find the complexity of the brute-force kNN algorithm and report it using big O notation. In which cases using kNN would not be a feasible solution?
4 Sentiment Analysis on Emails [50 pts]
As a computer scientist working for an online science magazine, your job is to analyze online data to classify mails from your subscribers according to their topics.
Data set
Your dataset is a preprocessed and modified version of 20 News Group Data Set [3]. It is based on 4000 real emails about 4 different topics in science. Emails have been preprocessed in the following ways:
• Stop word removal: Words like “and”,“the”, and “of”, are very common in all English sentences and are therefore not very predictive. These words have been removed from the emails.
• Removal of non-words: Numbers and punctuation have both been removed. All white spaces (tabs, newlines, spaces) have all been trimmed to a single space character
• Removal of infrequent words: Words that occur only once in all data set are removed from emails in order to reduce the size of the data.
3

The data has been already split into two subsets: a 3200-email subset for training and a 800-email subset for testing (consider this as your validation set and imagine there is another test set which is not given to you). Features have been generated for you. You will use the following files:
• question-4-train-features.csv • question-4-train-labels.csv
• question-4-test-features.csv • question-4-test-labels.csv
• question-4-vocab.txt
The files that end with features.csv contain the features and the files ending with labels.csv contain
the ground truth labels.
In the feature files each row contains the feature vector for an email. The j-th term in a row i is the occurrence information of the j-th vocabulary word in the i-th email. The size of the vocabulary is 37358. The label files include the ground truth label for the corresponding email (label 0 is medicine, label 1 is space, label 2 is cryptology and label 3 is electronics), the order of the emails (rows) are the same as the features file. That is the i-th row in the files corresponds to the same email. Each email is labeled as either cryptology, space, medicine or electronics.
The file ending with vocab.txt is the vocabulary file in which the j-th word (feature) in the file corresponds to the j-th feature in both train and test sets.
