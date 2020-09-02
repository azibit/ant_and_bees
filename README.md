# Starter for deploying [PyTorch](http://pytorch.org/) models on [Render](https://render.com)

This repo was originally for deploying FastAI models on Render. Now, we have modified the code to read Pytorch trained models and deploy on Render.

### Step 1: Build the Model
Run the following Google Colab to build a model you would be using: https://colab.research.google.com/drive/1HQCyAlKkdiT_48OoYsvqYxsurmYAIGqP?usp=sharing . This notebook contains a minimal code that only focuses on building the model. 

If you need more information about the model, you can check out this Google Colab
https://colab.research.google.com/drive/1IbzIbVE5CvPZ_Ni6ZSY3lBdD_dy5BPW2?usp=sharing


### Step 2: Save the Full Model Online
After training, save the model to a location online where you can get a link to it. My model is saved on Amazon S3 and here is my link: https://aidris559lab4.s3.amazonaws.com/Trained_Model_For_Ant_And_Bees/full_model_export1.pkl

### Step 3: Update server.py
Based on how we trained our model, we update a few code in the server.py file to use the transformation that was used to create our training and test images. We update the link to the saved model and also the name of the file containing the model. For me, my file name is full_model_export1.pkl


### Step 4: Update index.html
Update the index.html to match the classes you are predicting.

### Step 5: Now Use Render
When you visit the Render Website, create a new Web Service and link this project to Render. Every time you push to the master branch, a new deployment is done. And you get a link to the website once its done. Mine is at: https://ants-and-bees.onrender.com/

** Note: Because Render charges for deployment after a while, I would only have this project up for a while after which it might not be available. Feel free to reach out if you encounter any bugs.