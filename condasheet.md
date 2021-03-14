# Conda Virtual Env cheat sheet

#### Conda virtual env
----------------------
* Find available conda envs
	```bash
	conda env list
	```
* Create a conda virtual env using path prefix (all packages get installed inside the venv dir)
	```bash
	conda create --prefix /path/to/venv/destination
	```
* Create a conda virtual env using a name (gets installd under the default conda_home_dir/envs)
	```bash
	conda env create --file environment.yml
	```

	```bash
	conda create --name venvname
	```
* Removing a conda venv
	```bash
	conda remove --name venvname
	```
	```bash	
	conda remove --prefix /path/to/venv/destination
	```

#### Conda package management
-----------------------------
* Conda get list of packages in current environment 
	```bash
	conda list -n venvname
	```
	```bash 
	conda list --prefix /path/to/venv/destination
	```
* Conda export a list of all packages currently installed in venv
	```bash	
	conda env export > environment.yml
	```
* Conda export a list of packages you explicitly asked for
	```bash
	conda env export --from-history > environment.yml
	```
* Conda install packages
	* current active environment
		```bash
		conda install numpy
		```
	* specific environment
		```bash
		conda install --name venvname
		```
		```bash
		conda install --prefix /path/to/to/venv/destination
		```
	* install specific version
		```bash
		conda install scipy=0.15.0
		```
* Conda remove packages
	```bash
	conda remove --name venvname scipy
	```
	```bash
	conda remove --prefix /path/to/venv/destination scipy
	```
* Conda update packages
	```bash
	conda update scipy
	```
    
#### Conda meta
-----------------
* Conda shorten the venvname prompt
	```bash
	conda config --set env_prompt '({name})'
	```

