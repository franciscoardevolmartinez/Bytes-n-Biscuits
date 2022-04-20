# CHAMELEON Hands-on Session Neural Networks
This Repository gives all data and information that are needed to participate in the neural networks hands-on session of the first CHAMELEON school.

# Things to install before the session

Please install the following things before the session.

- Python 3
- Anaconda: this is the easiest way for all that is coming. If you don't have Anaconda already you can download it here: https://www.anaconda.com/products/individual </br>
- Jupyter Notebook: conda install -c conda-forge notebook</br> 

Also, the following packages are needed:
- SKlearn: conda install scikit-learn
- Keras/Tensorflow: conda install tensorflow
- numpy: conda install numpy
- matplotlib: conda install matplotlib
- corner: conda install -c conda-forge corner

Please contact us before the session if you have any problems. </br>

# General Idea

We prepared two different problems, which can be solved using Machine Learning. </br>

First problem:</br>
### Extracting exoplanet parameters using spectra.</br>
The goal here is to predict atmospheric parameters of exoplanets from their transmission spectra using machine learning.</br>
You will be provided with a dataset containing synthetic HST/WFC3 transmission spectra of exoplanets and their corresponding parameters.</br>
The parameters defining the forward models are: isothermal temperature; H2O, HCN and NH3 mixing ratios; and a grey cloud opacity.</br>
The spectra consist of 13 wavelength bins between 0.8 and 1.6 microns, which match those of the WASP-12b observation in Kreidberg et al., 2015.</br>
This observation is also provided to retrieve on once your machine learning algorithms have been trained.</br>

Second problem: </br>
### Emulating SED modelling of protoplanetary disks. </br>
The goal is to predict Spectral Energy distributions (SEDs) for protoplanetary disks based on disk parameters. </br>
The conventional way of predicting SEDs is to run a modelling code (ProDiMo, MCFOST, ..) to simulate a disk and then calculating how the output would look like.</br>
If you want to calculate a lot of SEDs this can take a lot of time. A potential solution for that problem is to train a Machine Learning algorithm to predict SEDs based on input parameters of disks. </br>
For doing that the algorithm must be trained on a large dataset of models, where the SED and the input parameters are known. </br>
This will be the DENT-grid (Kamp et al. 2011) in our case. </br> 
A detailed description of the data can be found in the folder data. </br>


### Questions to answer:
- Is it possible to solve your problem with machine learning?
- What is a good architecture/setting of your network?
- What happens if you train for more iterations?
- What happens if you use different scaler?
- How does the size of your data set influence your results?
- Can a Random Forest give better results?
...

# Steps
- Decide on a dataset you want to analyse.
- Set up a notebook 
- Import the needed packages
- Import the data
- Scale your data
- Import an ML technique and adjust it
- Analyse the results
- Start playing with different settings and techniques to find the best results

# Detailed Explanation

Set up a notebook in which you want to solve your problem. </br>
Windows: Open Anaconda Prompt and type in 'jupyter notebook'. This opens your browser. Go to the folder where you want to have your notebook and click on new+python3. </br>
Linux/Mac: Same steps as Windows but you open your terminal and your anaconda environment.


## 1: Loading your data

You find the data for your problem in the folder 'Data'. Click on the problem you want to tackle and download the data. </br>
(You can also download the whole repository to make things easier.) </br>
Load the data into your notebook. If you feel confident you can do this without further help. </br>
If you run into problems or want to check if you have done everything right, check out the load_data.ipynb. There you find a working version for loading the data.

## 2: Scaling your data

Once you loaded the data you have to scale it. </br>
In the folder 'Scaling' you find an explanation of different scaling methods and how to apply them.
Feel free to play around and visualize how your data is changing if you apply a scaler. </br>
Again, in the folder named after your problem, you find a working example of scaling the data. </br>


## 3: Applying Machine Learning

After loading and scaling your data, it is now time to apply some Machine Learning.</br>
We focus on Neural Networks in this session, but you can also run Random Forests as a comparison.</br>

### 3.1: Build/train a Neural Network

Depending on your level of confidence you can take different approaches.
- Have a look at the slides (Presentation.pdf), where a detailed explanation is given. </br>
  There are also a lot of links to more material if you have any questions. Also, google seems to be a python/NN expert.
- If you want to have more support look into the folder for your problem. There you will find an example of a suitable NN for your problem.

### 3.2: Optimize your network

If you have a working network, you can change the different settings and have a look at how your results change. Try to find the best network for your problem.

### 3.3: Optional: Build/ train a Random Forest

If your network works and you get bored, try to solve your problem using a different ML technique. </br>
We recommend Random Forest (a few hints can be found in the 'ML_techniques' folder), but you can also apply other methods. </br>
A list of methods can be found here: https://scikit-learn.org/stable/supervised_learning.html </br>

## 4: Visualization

This point is hard to separate from all previous steps. During the whole process you probably want to see what is going on. </br>
This is especially important, to evaluate your results. Think of useful ways to evaluate the results and visualize them. If you need a bit of inspiration, in the folder 'Visualization' there are a few useful tools.

# Other useful things

## .ipynb problems
If github has a problem with opening notebooks online there are two solutions for it.
- Download the repository and open it with your jupyter notebook
- Go to https://nbviewer.jupyter.org/github/tillkaeufer/chameleon_neural_network/tree/master/ </br>
  This is an independent site, where it should be possible to open all .ipynb files
  
## Complete notebooks
If nothing wants to work, in the folder 'Complete Notebooks' are working notebooks to solve both problems. You can just execute them and play around with the different hyperparameters.
