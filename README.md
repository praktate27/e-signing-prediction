# e-signing-prediction

# Problem Statement:
	Lending companies gives loan based on financial history of applicants. It is identified based on whether applicants will complete 
	the electronic process ie e_signing. 
# Goal
	Aim of project is about creating a model that predicts whether or not applicants will complete e_sigining phase of loan application.
	The lending companies will use this model to identify leass 'quality' applicants that is those who are not responding to onboarding process
	and experiment with giving them different onboarding screens.
# Data
	financial_data.csv has data including personal information like age, and time employed, as well as other financial metrics. These data points are used to create risk scores based on many different risk factors. Set of scores are built using some algorithms. Using this personal and financial features, we can predict if the user is more likely to respond to current onboarding process.
# Model Accuracies
	index Model 		          Accuracy    Precision    Recall     F1 Score
	0     Linear Regression (Lasso)	  0.561977    0.575963	   0.705913   0.634351
	1     SVM (Linear)		  0.568398    0.577769	   0.735996   0.647354
	2     SVM (RBF)			  0.591569    0.605720	   0.690871   0.645505
	3     Random Forest (n=100)	  0.621999    0.640137	   0.679979   0.659457
	4     Random Forest (n=100, GS*2
		+ Entropy)	          0.635399    0.646009	   0.713693   0.678167
	5     Random Foresh (n=100, GS*2 
	        + Gini)			  0.635120    0.649207	   0.700726   0.673984	
# Predictions (showing few records)
	entry_id	e_signed	predictions
	6493191		1.0			0
	6889184		1.0			1
	7048193		1.0			1
	6017637		0.0			1
	2718414		0.0			0
	1213384		1.0			1
# Conclusion
	Model has given us 64% of accuracy. Hence with help of that we can predict whether or not user will complete e-signing step of application. One way to levarage this model is to target those predicted to not reach e-sign phase with customized onboarding. This means that when applicant arrives, they may receive a different onboarding experience based on how likely they are to finish general onboarding process. This can help company to minimize how many people drop off from funnel. 
