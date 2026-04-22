# Installation instructions

#### Note: WiFi access for Cefas staff
If your laptop is configured to use the eduroam academic network this will be available across campus. Alternatively [register to Sky's free WiFi The Cloud](https://account.thecloud.eu/spportal/).


It is recommended to have python installed on your laptop. Nevertheless there are two alternatives:

* If you are unable to install python on your laptop, you can use the free cloud hosting service [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/ueapy/pythoncourse2026-materials/main?urlpath=lab). It will allow you to run all the lessons with the accompaigning data albeit with some limitations. It will be slower to start a session and run more involved examples, and it will not allow you to load your own data or save any changes made to the lessons.

* If you already have an account on the Ada High Performance Computing Cluster, then it would be possible to run the Jupyter notebooks of the lessons by starting a session on [Ada OnDemand](https://adaood01.uea.ac.uk/). You can try to follow the instructions below for copying and running the lessons, but we won't be able to provide support to get yourself setup.

## 1. Laptop Installation
For this course it is recommneded that you have Python installed on your laptop. Follow the instructions below to set up your Python environment with the required packages used in the lessons. Make sure you do this do this **before** the course, including running the test as below. There will be a troubleshooting session on the first day at 8:30 as advertised in the invite email.

Feel free to contact [Claire at Cefas](mailto:claire.beraud@cefas.co.uk) or [Alice at UEA](mailto:a.hsu@uea.ac.uk) if you have any problems with the installation (but better do an internet search first!)

### 1.1 Install Python distribution

#### Cefas Users
You will neet to request in advance a temporary administrator password to make the installation. 

As a government organisation we do not have free access to Anaconda, so please use the free alternative mambaforge. For those in academia, we also recommend this as a more lightweight (and often faster) python installation option!  

* [Download Mambaforge for your OS](https://github.com/conda-forge/miniforge#mambaforge) 

* After downloading, follow the instructions as suggested [here](https://github.com/conda-forge/miniforge#install)

#### Students or UEA Staff

* [Download Anaconda with Python 3 for your OS](https://www.anaconda.com/download/). 

* Install it following [these instructions](https://docs.anaconda.com/anaconda/install/). Be sure to select install "just me" when prompted.


### 1.2. Download course materials
From the Friday before the course (5th of June) the material for the workshop can be downloaded as a [zip file](https://github.com/ueapy/pythoncourse2026-materials/archive/main.zip) or can be cloned from our [GitHub repository](https://github.com/ueapy/pythoncourse2026-materials). 


#### 1.2.1. Option 1: Download ZIP file (easier)
Download the materials as a [zip file](https://github.com/ueapy/pythoncourse2026-materials/archive/main.zip) and unpack it in a suitable directory, for example, in `Downloads` folder. Jump to [1.3. Create the environment](#13-create-the-environment).

#### 1.2.2. Option 2: Using Git (allows restoring originals after modifications)
##### 1.2.2.1. Install Git
If you don't have git version control system installed, you can install it following these instructions:
###### Linux
Use your package manager. For example, using aptitude you would run the following terminal command: `sudo apt-get install git`
###### Mac
The XCode command line tools need to be installed.

* Install XCode if it isn’t already. XCode is available in the Mac App Store for free.
* Launch XCode and accept the license agreement.
* Quit XCode.
* Open a new terminal and run the command `xcode-select --install`
* Select install on the pop-up menu.

###### Windows
Download and install [Git for Windows](https://git-scm.com/downloads).

##### 1.2.2.2. Clone the repository

Open the command line (Git bash, terminal or cmd.exe)

(Linux or Mac, optional) Change to a suitable directory (e.g. `cd /home/yourname/Documents`)

Clone the repo by typing

```
git clone https://github.com/ueapy/pythoncourse2026-materials.git
```
This should create a local copy of the course materials in the current directory.

Windows-users, double check that it has been cloned in the directory you wanted.


### 1.3. Create the environment
* Make sure Anaconda or Mambaforge is installed and the course materials are downloaded

* Open the command line or python prompt (i.e., search "Terminal" on Mac Spotlight Seach; search "Anaconda prompt" or "mamba" on Windows start menu)

* Navigate to folder containing the cloned / downloaded course materials. Use the `cd` command, for example:

```
cd C:\Users\myname\Downloads\pythoncourse2026-materials\
```

* Create the environment using `conda` package manager:

```bash
conda env create -f environment.yml
```
or if you installed mamba
```bash
mamba env create -f environment.yml
```

This will take some time depending on your Internet speed (<15 minutes).


If you get stuck try typing return or, failing this, creating the environment again.

### 1.4. Test the installation (essential!)
#### Linux / Mac
If your default shell is NOT bash, first type `bash`. Type the following 2 commands:

```
conda activate course2026
python -c "import seaborn"
```
#### Windows
In the command line (Anaconda/mamba prompt), type the following 2 commands:

```
conda activate course2026
python -c "import seaborn"
```

If you don't get any errors then your installation was sucessful.

## 2. How to start Jupyter

Note: If you installed Anaconda (as opposed to the stripped down miniconda) you might want to try using the launcher application Navigator. You can learn how to start it for your OS (here)[https://docs.anaconda.com/free/navigator/getting-started/].


### Windows
* Open Anaconda/mamba prompt from your Start menu

* Type

```
conda activate course2026
jupyter lab
```

### Linux / Mac
* Open a terminal
* Type

```
conda activate course2026
jupyter lab
```


This should open Jupyter Lab in your browser. We will also demonstrate using Jupyter Notebook which is the older version with a simplified interface and is started with

```
jupyter notebook
```


## Still having trouble?
If you are unable to install Anaconda Python on your PC, contact the [course organisers](index.md#registration-and-enquiries).
Another option: launch the course in the cloud! [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/ueapy/pythoncourse2026-materials/main?urlpath=lab) This requires no installation but progress and modifications won't be saved.
