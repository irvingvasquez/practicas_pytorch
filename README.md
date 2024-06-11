# Prácticas de Pytorch


Pytorch es una librería reciente que se está esparciendo en la comunidad académina e industrial para desarrollar sistemas basados en aprendizaje automático, en especial en aprendizaje profundo. En este repositorio encontrarás una serie de ejercicios para aprender o reforzar tu conocimiento acerca de la implementación de redes neuronales profundas. Este repositorio es complemento al curso de introducción a las redes neuronales. Para más detalles visita mi página web.

Irving Vasquez
[Sitio Web]


## Configurar ambiente con conda

Para facilitar la instalación y ejecución de los ejercicios se utiliza de manejador conda. En dependencia de que distribución se use se puede llamar minicomda o anaconda. Para simplicidad en este repositorio se usa minconda.

De la definición de conda [docs](http://conda.pydata.org/docs):

> Conda is an open source package management system and environment management system for installing multiple versions of software packages and their dependencies and switching easily between them. It works on Linux, OS X and Windows, and was created for Python programs but can package and distribute any software.

### Pasos
Para tener los programas listos haremos dos cosas:

1. Install [`miniconda`](http://conda.pydata.org/miniconda.html) on your computer, by selecting the latest Python version for your operating system. If you already have `conda` or `miniconda` installed, you should be able to skip this step and move on to step 2.
2. Create and activate * a new `conda` [environment](http://conda.pydata.org/docs/using/envs.html).

\* Nota que cada que vayamos a usar los programas debemos de activar el ambiente de `conda`!

---

## 1. Instalación de miniconda

**Download** the latest version of `miniconda` that matches your system.

**NOTE**: There have been reports of issues creating an environment using miniconda `v4.3.13`. If it gives you issues try versions `4.3.11` or `4.2.12` from [here](https://repo.continuum.io/miniconda/).

|        | Linux | Mac | Windows | 
|--------|-------|-----|---------|
| 64-bit | [64-bit (bash installer)][lin64] | [64-bit (bash installer)][mac64] | [64-bit (exe installer)][win64]
| 32-bit | [32-bit (bash installer)][lin32] |  | [32-bit (exe installer)][win32]

[win64]: https://repo.continuum.io/miniconda/Miniconda3-latest-Windows-x86_64.exe
[win32]: https://repo.continuum.io/miniconda/Miniconda3-latest-Windows-x86.exe
[mac64]: https://repo.continuum.io/miniconda/Miniconda3-latest-MacOSX-x86_64.sh
[lin64]: https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh
[lin32]: https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86.sh

**Install** [miniconda](http://conda.pydata.org/miniconda.html) on your machine. Detailed instructions:

- **Linux:** http://conda.pydata.org/docs/install/quick.html#linux-miniconda-install
- **Mac:** http://conda.pydata.org/docs/install/quick.html#os-x-miniconda-install
- **Windows:** http://conda.pydata.org/docs/install/quick.html#windows-miniconda-install

## 2. Crear y activar el ambiente

For Windows users, these following commands need to be executed from the **Anaconda prompt** as opposed to a Windows terminal window. For Mac, a normal terminal window will work. 

#### Git and version control
These instructions also assume you have `git` installed for working with Github from a terminal window, but if you do not, you can download that first with the command:
```
conda install git
```


**Now, we're ready to create our local environment!**

1. Clone the repository, and navigate to the downloaded folder. This may take a minute or two to clone due to the included image data.
```
git clone https://github.com/irvingvasquez/practicas_pytorch.git
cd practicas_pytorch
```

2. Create (and activate) a new environment, named `pptorch` with Python 3.7. If prompted to proceed with the install `(Proceed [y]/n)` type y.

	- __Linux__ or __Mac__: 
	```
	conda create -n pptorch python=3.7
	source activate pptorch
	```
	- __Windows__: 
	```
	conda create --name pptorch python=3.7
	conda activate pptorch
	```
	
	At this point your command line should look something like:

	`(pptorch) <user>:practicas_pytorch <user>$`. 
	
	The `(pptorch)` indicates that your environment has been activated, and you can proceed with further package installations.

3. Install PyTorch and torchvision; this should install the latest version of PyTorch. Mi recomendación es revisar antes la [documentación oficial](https://pytorch.org/get-started/locally/) de pytorch y verificar los comandos en dependencia de si se va a utilizar GPU o no. Los siguientes comandos son para usar CPU.
	
	- __Linux__ or __Mac__: 
	```
	conda install pytorch=1 torchvision cpuonly -c pytorch
	```
	- __Windows__: 
	```
	conda install pytorch=1 torchvision cpuonly -c pytorch
	```

6. Install a few required pip packages, which are specified in the requirements text file (including OpenCV).
```
pip install -r requirements.txt
```

7. That's it!

Now all of the `pptorch` libraries are available to you. Assuming you're environment is still activated, you can navigate to the Exercises repo and start looking at the notebooks:

```
cd
cd practicas_pytorch
jupyter notebook
```

To exit the environment when you have completed your work session, simply close the terminal window.

Referencias usadas:
Udacity, Deep Learning with PyTorch

[Sitio Web]: <https://jivasquez.wordpress.com/>
