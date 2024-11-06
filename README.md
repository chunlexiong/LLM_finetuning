# LLM fine-tuning

This repo does fine tuning of LLM using e-commence data. The base model is "sentence-transformers/all-MiniLM-L6-v2", and the dataset used for fine-tuning is [Home Depot](https://huggingface.co/datasets/Ukhushn/home-depot). 

To run the notebook "llm_ecommerce.ipynb", please follow the steps below:

* run "git clone https://github.com/chunlexiong/LLM_finetuning.git" to have a copy of this repo to your computer. If this doesn't work due to access issue, you may want to fork it to your own github account first
* install python 3.11 on your computer and create a virtual environment by running "python -m venv your_vm_folder_name --copies" in terminal if it is MacOS, or "python -m venv your_vm_folder_name" in terminal if it is Windows.
* activate the virtual environment by "source your_vm_folder_name/bin/activate" (MacOS)
* get into the repo folder, run "pip install -r requirements.txt"
* after the python package dependencies installation finishes, run "pip list" to double check numpy==1.26.4, sentence-transformers==3.1.1, and transformers==4.45.2. We need those slightly older versions because Pytorch doesn't work with latest numpy, and the latest transformers have a bug when computing losses.
* use jupyter notebook to open the llm_ecommerce.ipynb file and test it out. Remember to modify the directory path where the models and checking points are saved to and loaded from.

Please note that without a GPU, it may take more than 10 hours to finish running the entire notebook. This won't work with Apple silicon GPU chips.
