# Adversarial_attack_and_defense_Machine_Learning_Project

Fast Gradient Sign Method Attack

FGSM is a white box attack whose goal is to ensure misclassification. This attack works on the following equation:

x_{adversarial} = x + epsilon*sign(cost function)

We  multiply  the  small  value to  the  signed  gradient  toensure that the perturbations are small enough that humaneye cannot detect them but large enough that they can foolthe network.The formulae is related to the gradient of thecost function just to increase the model error.
