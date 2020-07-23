### Build an American Sign Language alphabet classifier using pytorch and GPU environments on Watson Studio


# Overview

we will use PyTorch to build and train a deep learning model to classify images to 29 classes (26 ASL alphabet, space, Del, and nothing) which can be used later to help Deaf peope communicate with other and maybe with computers as well. We will use a pre-trained mobile network and we will define our classifier and connect it to network, then train this classifier along with some of the last blocks of the network on our dataset.

In this notebook we will:

1- Obtain dataset from Kaggle.  
2- explore data and define transformers to preprocess images before training.  
3- define our classifier to have an output layer of 29 outputs.  
4- train the last blocks of the network along with the classifier we defined.  
5- test the model we trained.  

This notebook uses python 3.6 + GPU environment which allow us to do the whole process and train complex model in the same place which is a notebook in Watson studio.
Learn more about available environments <a href="https://dataplatform.cloud.ibm.com/docs/content/wsj/analyze-data/gpu-environments.html"> Watson Studio environments.</a>




# Flow

    

![Flow](https://raw.githubusercontent.com/IBM/ASL-Pytorch/master/images/diagram.png)

1. Log into IBM Watson Studio.
2. Get your Kaggle API credentials
3. Run the Jupyter Notebook in Watson Studio.

# Instructions


1. [Sign up for Watson Studio](#1-sign-up-for-watson-studio)
2. [Create a new project](#2-create-a-new-project)
3. [Create the notebook](#3-create-the-notebook)
4. [Run the notebook](#6-run-the-notebook)
5. [Test your model](#7-Test-the-model)

### 1. Sign up for Watson Studio

We will use Watson studio to run this notebook, Watson studio is available through IBM cloud or IBM Cloud Paks For Data.

* To start you must have IBM cloud account, Get your for free <a href="https://cloud.ibm.com/registration">Here.</a>   
* From the catalog create a <a href="https://cloud.ibm.com/catalog/services/watson-studio">watson studio</a> with standard plan or more and make sure the region is dallas to enable GPU environment.  

![CREATE WS](https://raw.githubusercontent.com/IBM/ASL-Pytorch/master/images/create.gif)  

### 2. Create a new project


From the Watson Studio home page, select `Creat a project`, then select the `Create an empty project` and choose a name for your project then press create .

![CREATE Project](https://raw.githubusercontent.com/IBM/ASL-Pytorch/master/images/project.gif)  

* create a watson studio project <a href="https://www.youtube.com/watch?v=-CUi8GezG1I">see tutorial here.</a>  

### 3. Create the notebook 

* create a new notebook from watson studio with GPU support.    
    * the notebook should have a GPU support <a href="https://www.youtube.com/watch?v=RNIWtpnNBoo">click here to learn how to create a notebook with GPU support.</a>
    * Use the From URL option and use this URL: https://github.com/IBM/ASL-Pytorch/blob/master/ASL_v2.ipynb

![NOTEBOOK](https://raw.githubusercontent.com/IBM/ASL-Pytorch/master/images/notebook.gif)

### 4. Run the notebook 

To view your notebooks, select `Notebooks` in the project `Assets` list. To run a notebook, simply click on the `edit` icon listed in the row associated with the notebook in the `Notebooks` list.

![ASL notebook](https://github.com/IBM/ASL-Pytorch/blob/master/images/note.png)

Follow notebook instructions to load data and train the model.  

Cells are how notebooks are structured and are the areas where you write your code. To run a piece of code, click on the cell to select it, then press `SHIFT+ENTER` or press the play button in the toolbar above. Additionally, the Cell dropdown menu has several options to run cells, including running one cell at a time or to run all cells at once.

### 4. Test the model

The last two cells in the notebook is where we test our trained model.
run the last model many times to check different samples.

![Result](https://github.com/IBM/ASL-Pytorch/blob/master/images/result.png)


### check notebook result 

[Notebook with outputs](https://github.com/IBM/ASL-Pytorch/blob/master/ASL_v2.ipynb)  

# Components and services


* Watson studio
* Jupyter Notebook
* Pytorch

# Runtimes


* Python
* Pytorch

# Related IBM Developer content

* [Get started with PyTorch ](https://developer.ibm.com/articles/cc-get-started-pytorch/): In this article, you can find an overview of the PyTorch system and learn more about the supported platforms and the benefits of using PyTorch.

* [Build models using Jupyter Notebooks in IBM Watson Studio](https://developer.ibm.com/technologies/artificial-intelligence/tutorials/watson-studio-using-jupyter-notebook/)
 

# Related links


* [Pytorch](https://pytorch.org/): learn more about pytorch
* [Create Watson Studio Notebooks](https://dataplatform.cloud.ibm.com/docs/content/wsj/analyze-data/creating-notebooks.html)
* [Learn more about GPU environments](https://dataplatform.cloud.ibm.com/docs/content/wsj/analyze-data/gpu-environments.html)


