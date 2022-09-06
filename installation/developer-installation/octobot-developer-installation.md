---
description: Setting up the recommended OctoBot development environment
---

# OctoBot developer installation

{% hint style="info" %}
This page is referring to OctoBot in versions superior to 0.4.0.
{% endhint %}

* [**Install OctoBot requirements**](octobot-developer-installation.md#install-octobot-requirements)
* [**Cloning OctoBot repositories**](octobot-developer-installation.md#cloning-octobot-repositories-with-git)
* [**Setting up the IDE**](octobot-developer-installation.md#setting-up-the-ide)
* [**create starting scripts in pyCharm**](octobot-developer-installation.md#create-starting-scripts-in-pycharm)
* [**start OctoBot in pyCharm**](octobot-developer-installation.md#start-octobot-in-pycharm)

## Install OctoBot requirements

**Download and install:**

* IDE: [PyCharm](https://www.jetbrains.com/pycharm/)
* SCM: [Git](https://git-scm.com/downloads)
*   we also use [GitKraken](https://www.gitkraken.com/git-client) to easily manage

    OctoBot's multiple repos, this is just a quality of life

    improvement and is not necessary.
* Language: [Python 3.8](https://www.python.org/downloads/release/python-3810/)

#### additional dependencies for Windows

* download [Visual Studio build tools](https://visualstudio.microsoft.com/downloads/#build-tools-for-visual-studio-2019) and install "Desktop development with C++"

![](<../../.gitbook/assets/image (9).png>)

![](<../../.gitbook/assets/image (5).png>)

#### additional dependencies for Mac

* install [GCC](https://discussions.apple.com/thread/8336714)

## OctoBot repositories

### Cloning OctoBot repositories with git

* open a terminal in your project folder and execute the following commands to download the repos

```bash
git clone --branch dev https://github.com/Drakkar-Software/OctoBot.git
git clone --branch dev https://github.com/Drakkar-Software/OctoBot-Tentacles.git
git clone https://github.com/Drakkar-Software/OctoBot-Trading
git clone https://github.com/Drakkar-Software/OctoBot-evaluators
git clone https://github.com/Drakkar-Software/OctoBot-Services
git clone https://github.com/Drakkar-Software/OctoBot-Backtesting
git clone https://github.com/Drakkar-Software/OctoBot-Tentacles-Manager
git clone https://github.com/Drakkar-Software/OctoBot-Commons
git clone https://github.com/Drakkar-Software/Async-Channel
git clone https://github.com/Drakkar-Software/trading-backend
```

* now you should have all the OctoBot repos in one folder

![](<../../.gitbook/assets/image (16).png>)

### Manage repositories with GitKraken

* open each folder in GitKraken

![](<../../.gitbook/assets/image (17).png>)

* add your project directory (the folder where all repo folders are located)

![](<../../.gitbook/assets/image (19).png>)

* now add each folder

![](<../../.gitbook/assets/image (10).png>)

* Now you have all repositories open as tabs and you can switch between branches

### switch to experimental branches

* You can explore and switch to different branches by double-clicking on the branch name for each repository, or right click "reset to this commit".

![](<../../.gitbook/assets/image (27).png>)

## Setting up the IDE

We recommend using [PyCharm](https://www.jetbrains.com/pycharm/) to navigate through the OctoBot projects. This IDE will allow you to open and navigate through the multiple OctoBot repositories and make your OctoBot run setup use the code directly from the cloned repos using the project dependencies.

* Open Pycharm and open the folder where all the OctoBot repositories are.

### Add Python interpreter

1. click on "\<No interpreter>"
2. then click on "Add Interpreter..."

![](<../../.gitbook/assets/grafik (2).png>)

1. select "Virtualenv Environment"
2. select the location of your venv. This should be your OctoBot project folder with "/venv" at the end
3. select your base interpreter and make sure its python 3.8 or 38

![](<../../.gitbook/assets/grafik (1).png>)

### Add OctoBot modules

This will allow your PyCharm python runner to use your OctoBot repositories as source code directly. Thanks to this you will be able to edit any file in any repo and it will be taken into account in your other PyCharm run profiles runners from other open OctoBot repo. This is useful when running tests. If you skip this, you will need to install every OctoBot module with pip and won't be able to edit their code.

### Add OctoBot modules with PyCharm Pro

*   In File/Settings/Project/Python Dependencies: For each repository: check its required OctoBot repository dependency.



    <figure><img src="https://raw.githubusercontent.com/Drakkar-Software/OctoBot/assets/wiki_resources/python_dependencies.png" alt=""><figcaption></figcaption></figure>

### Add OctoBot modules with PyCharm Community

Go to File -> Settings and add your OctoBot module folders as a project source

<figure><img src="../../.gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>

### Install Octobot dependencies

* For each OctoBot's repository: install missing dependencies in requirements.txt and dev\_requirements.txt

```
pip install -r OctoBot/requirements.txt
pip install -r OctoBot-Backtesting/requirements.txt
pip install -r OctoBot-Commons/requirements.txt
pip install -r OctoBot-evaluators/requirements.txt
pip install -r OctoBot-Services/requirements.txt
pip install -r OctoBot-Tentacles-Manager/requirements.txt
pip install -r OctoBot-Trading/requirements.txt
pip install -r Async-Channel/requirements.txt
pip install -r trading-backend/requirements.txt

pip install -r OctoBot-Backtesting/dev_requirements.txt
pip install -r OctoBot-Commons/dev_requirements.txt
pip install -r OctoBot-evaluators/dev_requirements.txt
pip install -r OctoBot-Services/dev_requirements.txt
pip install -r OctoBot-Tentacles-Manager/dev_requirements.txt
pip install -r OctoBot-Trading/dev_requirements.txt
pip install -r OctoBot-Trading/dev_requirements.txt
pip install -r trading-backend/dev_requirements.txt
```

{% hint style="warning" %}
Through the requirements you have also installed OctoBot packages related to the previously downloaded repositories. You must uninstall them or your python runner will use them instead of your local code version.
{% endhint %}

* remove OctoBot pip packages to use the packages from your project directory

```
pip uninstall -y OctoBot-Backtesting OctoBot-Trading Async-Channel OctoBot-Evaluators OctoBot-Commons OctoBot-Tentacles-Manager OctoBot-Services trading-backend
```

## create starting scripts in pyCharm

Create PyCharm run configurations using the previously created virtual env (with all the dependencies installed) for each way you want to start python commands (running OctoBot, running tests, etc).

### Introduction into OctoBot scripts

{% hint style="info" %}
Here we explain how to setup and run two scripts for OctoBot, but there are way more you can set up by yourself, explore the rest of the docs to find out more commands
{% endhint %}

* ****[**OctoBot starting script**](octobot-developer-installation.md#octobot-starting-script)****
* ****[**install OctoBot-Tentacles and run OctoBot script**](octobot-developer-installation.md#install-octobot-tentacles-and-run-octobot-script)****

### OctoBot starting script

{% hint style="info" %}
this script will run OctoBot and apply all changes made to all repositories except the OctoBot-Tentacles folder (see [install OctoBot-Tentacles and run OctoBot script](octobot-developer-installation.md#install-octobot-tentacles-and-run-octobot-script))
{% endhint %}

* click on Add Configuration

![](<../../.gitbook/assets/image (26).png>)

now add a new python script

![](../../.gitbook/assets/image.png)

### Start OctoBot in pyCharm

* You can now run and debug the whole OctoBot project and its repositories by clicking on the play button, or on the debugging button to run the debugger

<figure><img src="../../.gitbook/assets/grafik.png" alt=""><figcaption></figcaption></figure>

### install OctoBot-Tentacles and run OctoBot script

{% hint style="info" %}
this script will install the OctoBot-Tentacles folder and run Octobot with all your changes applied from all repositories.
{% endhint %}

#### Create the following three scripts:

* \*\*Script to create an installable OctoBot-Tentacles package \*\*

![](<../../.gitbook/assets/image (20).png>)

* **Script to install OctoBot-Tentacles package**

![](<../../.gitbook/assets/image (25).png>)

* **Script to zip, install and run in one go**

![](<../../.gitbook/assets/image (12).png>)