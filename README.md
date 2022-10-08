#  Diffusion Models Homework


In this assignment you will become familiar with the basic concepts of diffusive models. Although the models corresponding to the state of the art require a very high computational power, there are simple implementations that we will use to analyze the image generation.


![diffusion-model image](diffusion.png)

## PART 1: Forward Diffusion

As seen in the class, the same amount of noise is not added at each step of the foward process. This amount of noise is regulated by a schedule wich scales the mean and the variance. This ensures that the variance doesn't explode as we add more noise.


Your task is to test new functions in order to keep the distribution as structured as possible for as many steps as possible. For a function you should analyze and explain the reasons for the results obtained.

In the utils.py file you can find the function where you can add different shedules.
This part can be done in your own computers.

## Requirements

* Python >= 3.7
* pytorch >= 1.6
* CUDA Toolkit
* GPU



## References 

Sohl-Dickstein, J., Weiss, E. A., Maheswaranathan, N., & Ganguli, S. (2015). Deep unsupervised learning using nonequilibrium thermodynamics. arXiv preprint arXiv:1503.03585. 

Max Welling & Yee Whye Teh. “Bayesian learning via stochastic gradient langevin dynamics.” ICML 2011. 

Ho, J., Jain, A., & Abbeel, P. (2020). Denoising diffusion probabilistic models. arXiv preprint arXiv:2006.11239.  

Prafulla Dhariwal, Alex Nichol, Diffusion Models Beat GANs on Image Synthesis, arXiv: 2105.05233 








