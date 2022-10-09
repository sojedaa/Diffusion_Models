#  Diffusion Models Homework


In this assignment you will become familiar with the basic concepts of diffusion models. Although the models corresponding to the state of the art require a very high computational power, there are simple implementations that we will use to analyze the image generation.




## PART 1: Forward Process (1.5 points)

As seen in the class, the same amount of noise is not added at each step of the foward process. This amount of noise is regulated by a schedule wich scales the mean and the variance. This ensures that the variance doesn't explode as we add more noise.

![diffusion-model image](diffusion1.png)

Your task is to test new schedule functions in order to keep the distribution as structured as possible for as many steps as possible. For a function you should analyze and explain the reasons for the results obtained.

In the utils.py file you can find the function where you can add different shedules.
This part can be done in your own computers.

## Requirements

* Python >= 3.7
* pytorch >= 1.6
* CUDA Toolkit
* GPU

## PART 2: Reverse Process (1 point)

a. Look at the code in the ddpm.py file and based on the theory explain the training and sampling algorithms for the reverse diffusion process. (0.5 points) 
b. For the both training and smampling algorithms find the comments #Start and #End and describe in detail what is happening in each line. (0.5 points)

## PART 3: Classifier Free Guidance (2.5 points)

1. Train the ddpm.py model for the StanfordCars dataset and save the results. Choose a number of epochs between 50 and 100 and save the images. (0.5 points)

2. Check the comments #2.item on the code. (0.4 pints each item)

a. Include a label embedding for the classes by adding some modifications to the module architecture (UNet) in the file modules.py. (Hint: Do not implement the architecture from scratch, create a new class for the conditional UNet).

b. In the ddpm_conditional.py file pass the labels of the dataloader to the new model. Choose a rate to train unconditionally and modify the sampling algorithm in the Diffusion class to implement Classifier Free Guidance.

c. Train the ddpm_conditional.py model for the StanfordCars dataset and save the results.

d. Compare the best results of the conditional and the unconditional models and analize the results. For the analysis explain how the Classifier Free Guidance works. If the results were not the expeceted explain why could have this happened.

e. Explain in your words what process should be the process to implement Classifier Guidance instead of Classifier Free Guidance.

## References 

Sohl-Dickstein, J., Weiss, E. A., Maheswaranathan, N., & Ganguli, S. (2015). Deep unsupervised learning using nonequilibrium thermodynamics. arXiv preprint arXiv:1503.03585. 

Max Welling & Yee Whye Teh. “Bayesian learning via stochastic gradient langevin dynamics.” ICML 2011. 

Ho, J., Jain, A., & Abbeel, P. (2020). Denoising diffusion probabilistic models. arXiv preprint arXiv:2006.11239.  

Prafulla Dhariwal, Alex Nichol, Diffusion Models Beat GANs on Image Synthesis, arXiv: 2105.05233 








