# Experiment title

PatentMatch Classification with LLama 3 - 8B

Reynold Oramas 

31-05-2024

## Goal of the experiment

1. On-hands discovery of the PatentMatch dataset, obtaining very preliminary baseline quality on the claim&cited-paragraph classification task (2 texts on model input, one binary classification label on output).

2. Learn how to use the newly introduced standards for implementation of research experiments.

# Developer Enviroment

### Information for exact reproductivity.

Working on a RunPod Pod with RTX 6000, template: "RunPod Pytorch 2.2.0" that has pytorch:2.2.0-py3.10-cuda12.1.1-devel-ubuntu22.04. With 128 Gb on container and disk space.

To connect RunPod to VSCode for development follow this blog https://blog.runpod.io/how-to-connect-vscode-to-runpod/.

After connected it is needed to install Python and Jupyter VSCode extensions on the remote machine.

### Install miniconda on linux

```
mkdir -p ~/miniconda3
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda3/miniconda.sh
bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3
rm -rf ~/miniconda3/miniconda.sh
```

After installation init miniconda

```
~/miniconda3/bin/conda init bash
~/miniconda3/bin/conda init zsh
```

Restart the terminal

Clone the repo
```
git clone https://github.com/HumanDevIP/reynold-experiments.git
```

Go to the repo folder 

```
cd reynold-experiments
```

Create the enviroment

```
conda create -p ./env python=3.10 -y
```

Activate enviroment

```
conda activate ./env
```

Select the created enviroment as the kernel for the notebooks.

### Follow from this step on for local or Jupyter enviroment development.

Install dependencies for data processing

```
pip install -r requirements_data.txt
```

Install dependencies for training

```
pip install -r requirements_train.txt
```

Create a .env file following the example.env with a Hugginface access token (Write) and MLFlow credentials.

### Code

In notebooks:

Data Processing: eda.ipynb

Model training: llama3_seq_class.ipynb
 
### Data

In the data folder exists the original data and the transformed folder with the data saved following the EDA notebook.

  
