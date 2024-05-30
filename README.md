# Install miniconda 
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

Create the enviroment
```
conda create -p ./env python=3.10 -y
```

Activate enviroment

```
conda activate ./env
```

Install dependencies for data processing
```
pip install -r requirements_data.txt
```

Install dependencies for training
```
pip install -r requirements_train.txt
```

# Experiment title 

The corresponding <a href:=https://www.notion.so/Plan-of-Experiment-PoE-template-efed4153dd7849c5979e9abb00293ec0>Plan of Experiment is provided here</a>.
\
The <a href:=https://www.notion.so/Experiment-Report-Template-450e66b444c74039bd1beda4f6c226a9>Full Report</a> describing the effort is also available.

## Goal of the experiment
Do provide project goal from the PoE document.

## A long section about how to run the code, examples of use, requirements, and similar.
Do provide a bullet-proof description so that a person who never used this code will know how to get started.

```
Specifically, do provide a section with information how to copy the repository.
git clone git@github.com:HumanDevIP/Experiment-repository-template.git
```

Also, state python version, and the compute environment where the code was executed (Ubuntu 22.04.LTS at a local machine, AWS EC2, and similar).

## Data
Do provide a description of how to obtain the necessary data. Specifically, do not store data files larger than 1 MB in the data folder.

## Credentials
Remember to provide all credentials, keys in the .env file only. This file is ignored in .gitignore already.  
The `example.env` file is a placeholder to demonstrate what credential keys are needed and should be pushed into the repository.  
