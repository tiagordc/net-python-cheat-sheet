# Conda

Command line package and environment manager

| Command | Description |
| --- | --- |
| conda info | check conda version |
| conda update conda | software update |
| conda install PACKAGENAME | install a package |
| conda update PACKAGENAME | update a package |
| conda create --name py35 python=3.5 | create a new environment named py35, install Python 3.5 |
| conda create --clone py35 --name py35-2 | make exact copy of an environment |
| activate py35 | Windows activate environment |
| deactivate | Windows deactivate environment |
| source activate py35 | Linux activate environment |
| source deactivate | Linux deactivate environment |
| conda env list | list all environments |
| conda list | list all packages and versions installed in active environment |
| conda list --revisions | list the history of each change to the current environment  |
| conda install --revision 2 | restore environment to a previous revision |
| conda list --explicit > requirements.txt | save environment to a text file  |
| conda env create --file requirements.txt  | create environment from a text file |
| conda env remove --name bio-env | delete an environment and everything in it  |
