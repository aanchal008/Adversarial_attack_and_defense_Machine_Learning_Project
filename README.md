# Adversarial_attack_and_defense_Machine_Learning_Project

Fast Gradient Sign Method Attack

FGSM is a white box attack whose goal is to ensure misclassification. This attack works on the following equation:

x_{adversarial} = x + epsilon*sign(cost function)

We  multiply  the  small  value to  the  signed  gradient  toensure that the perturbations are small enough that humaneye cannot detect them but large enough that they can foolthe network.The formulae is related to the gradient of thecost function just to increase the model error.

-----------------------------------------------------------------------------------------------------------------------------------------------

Projected Gradient Descent

This is also know as Iterative Fast gradient sign method(I-FGSM). The key to understand PGD attack is frame findingan adversarial example as constrained optimization.  It at-tempts to find the perturbation that maximizes the loss ofa model on a particular input, while keeping the size ofthe perturbation smaller than a specified amount which is epsilon.

The idea here to find the adversarial example is to maximizeover the set of images that are very close to x maximizing the cross entropy loss of our neural network evaluated atthe perturbed network with respect to the true label. Here,maximizing the cross entropy loss means fooling the neuralnetwork.

-----------------------------------------------------------------------------------------------------------------------------------------------

Defense Distillation

It is a gradient masking technique in which we try to hidethe gradient information of the model so as to confuse the adversaries.

The algorithm successfully works and protect against theattack. The biggest advantage of this algorithm is that it isadaptable to unknown threats. The algorithm trains the firstmodel to predict the output probabilities of second model.Typically, smaller network learns another network’s outputfunction. But instead of predicting the hard class labels, thedistilled network predicts the class probabilities generatedby the first network.  It trains the model at temperatureTbut test it at temperatureT=1.  This cause the input tosoftmax to become larger by a factor ofT. This will causethe softmax function to output the class target score closeto 1 while other classes have score close to 0.  This wayattacker cannot find the gradient score function F.

The defense techniques that perform the gradient maskingresult in a model which is smooth in specific directions andneighbourhood of the training points. This makes it harderfor the adversary to find the gradient direction to perturb theinput in harmful way for the model.

