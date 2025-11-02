# Combing Convolutional Neural Network with Large Language Models and Evolutionary Algorithms to Optimise Deepfake Image Detection on Social Media
This GitHub repository contains the full code for the dissertation "Combing Convolutional Neural Network with Large Language Models and Evolutionary Algorithms to Optimise Deepfake Image Detection on Social Media" as one consolidated Jupyter Notebook file.

The code pipeline is divided in five parts that are explained in the following:

**1. Download and Setup of the WildDeepfake Dataset**  
This part of the pipeline downloads the WildDeepfake dataset and sets it up to be used in parts 3, 4 and 5.

**2. Download and Setup of the Celeb-DF v2 dataset**  
This part of the pipeline downloads the Celeb-DF v2 dataset and sets it up to be used in parts 3, 4 and 5.

**3. Training and Evaluation of Basic CNN for Deepfake Detection**  
Here, the basic standalone CNN gets trained on the WildDeepfake dataset and cross-validated against the Celeb-DF v2 dataset it did not see during training. The result is used as baseline to measure the improvements made by the two LLM-supported evolutionary algorithms.

**4. First LLM-supported Evolutionary Algorithm**  
This code pipeline runs through an LLM-supported evolutionary algorithm (EA) to improve the basic standalone CNN's capability to generalise to the Celeb-DF v2 dataset without seeing its data during training. For that, an evolutionary search is conducted which searches through different CNN architecture choices and parameters.

**5. Second LLM-supported Evolutionary Algorithm**  
Here, the best evolved basic CNN from the fourth step is taken and fused with a Vision Language Model (VLM). Prompt Engineering is conducted to get the VLM to detect deepfakes as good as possible. Then, the second LLM-supported EA conducts a search on the best way to fuse the CNN that was derived in the first LLM-supported EA with a VLM model to improve the overall accuracy on both datasets as much as possible.

**Some additional remarks**  
To get this code running, the user must have a Google Cloud Platform account. Then, the Google Cloud Console must be opened. It must be navigated to "Vertex AI" and then to "Notebooks" and "Workbench". There, a Workbench Instance must be created. It is necessary to choose an instance that has GPU access. Once it is set up, JupyterLab can be opened through the instance. There, the Jupyter Notebook file can be uploaded and opened.  
Within the Jupyter Notebook file, the user must input some information into the code. The Google Cloud Storage bucket and OpenAI API key used for the dissertation were exchanged with "???" in the code. There, the user must input their information.  
Following these steps, the user is able to run the code related to the dissertation and replicate its findings.
In some of the cells' outputs, errors are shown. None of these are important as they are only related to unimportant parts of the code like, e.g., Google Cloud Storage uploads of results. All important parts of the code run through successfully.






