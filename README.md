# Instructions for running the Jupyter notebook LLM_workshop.ipynb

The notebook uses Python 3. It is recommended to run it in an Anaconda virtual environment.  


## Creating and activating a virtual environment

If you do not have Anaconda/Miniconda installed, you can install it here:  
    https://conda.io/projects/conda/en/latest/index.html

Run the following commands in your Terminal (Linux/Mac) or command line (Windows):  

Make Anaconda virtual environment (called "llm") with Python 3:  
    ```conda create -n llm python=3```

Activate the virtual environment:  
    ```conda activate llm```

Run all the commands below in this virtual environment. (It needs to be activated whenever a new terminal window is opened.)


## Installing Python packages

PyTorch is by default run with CUDA for using GPU computation. However, a CPU-only version is also available.

Alternative 1: GPU version of PyTorch (CUDA=11.8):  
    ```pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118```

Alternative 2: CPU-only version of PyTorch:  
    ```pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cpu```

(Note: Parts 1--2 of the notebook work with both GPU and CPU versions, but Part 3 requires GPU.)

Install Transformers, SentenceTransformers, and Jupyter:  
    ```pip install --upgrade huggingface_hub transformers accelerate peft bitsandbytes trl tensorboardX sentence-transformers jupyter```


## Downloading dataset

Part 1 of the notebook uses a dataset called spamdata_v2.csv, available here:  
    https://github.com/prateekjoshi565/Fine-Tuning-BERT/blob/master/spamdata_v2.csv

Click on "Download raw file" (on the right-hand side), and save it to the same folder as the notebook.


## Starting Jupyter notebook

From the terminal, run:  
    ```jupyter notebook```

This should open a browser window showing a folder with files, including LLM_workshop.ipynb.  
Double-click on the file to open the notebook.
