# Optimization

To set your work environment with conda, create a virtual env "v_env_name", then install ipykernel and the requirement.txt file.
Bellow a list of useful command.

```terminal
#conda needed

#Create new virtual env
conda create -n v_env_name python=3.10

#Activate virtual env
conda activate v_env_name

#Install all future needed python packages
conda install ipykernel flake8

conda install -n v_env_name --file requirements.txt
pip install -r requirements.txt

#remove conda env
conda env remove -n v_env_name

#Add Jupyter kernel (may need sudo)
python -m ipykernel install --name v_env_name

#Sup Jupyter kernel
jupyter kernelspec uninstall v_env_name

#Run Jupyter lab
jupyter lab

#Create new jupyter kernel
python -m ipykernel install --user --name v_env_name --display-name "v_env_name"

#Run Fastapi with uvicorn
uvicorn ml_api:app --reload

#Postman is used to manage API requests

#pipreqsnb (pipreqs with notebook) is used to generate requirements.txt file, missing :
jupyter, ipykernel, uvicorn, (some libs related to plotly (see error msgs))
```