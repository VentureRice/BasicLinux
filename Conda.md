新建conda环境
```shell
conda create --name yourEnv python=3.7
conda activate yourEnv
conda install jupyter
conda list
```
添加到jupyter
```shell
conda install nb_conda
pip install ipykernel
python -m ipykernel install --user --name yourEnv --display-name "yourEnv"
```
