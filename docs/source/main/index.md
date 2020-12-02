# <span style="color:green">INTRODUCTION</span>

## Overview

The aim of this documentation is to provide a step-by-step guide for users of Odor2Action (O2A) data and centralized computing resources. The data storage and computing resources are hosted by CU Research Computing (CURC). This documentation should help you get started with most tasks, however you can refer to the [main CURC documentation page](https://curc.readthedocs.io) for additonal information.

The following schematic may be useful for visualizing CURC resources: 

![](images/o2a_overview.png)

__Resources__: The following computing and storage resources are available to O2A users:

1. The dedicated O2A compute node on the <a href="https://www.colorado.edu/rc/resources/blanca" target="_blank">Blanca condo cluster</a> (most computing tasks)
2. Shared computing nodes on the <a href="https://www.colorado.edu/rc/resources/summit" target="_blank">RMACC Summit supercomputer</a> (very big computing tasks)
3. The <a href="https://www.colorado.edu/rc/resources/enginframe" target="_blank">CURC EnginFrame ("Viz") cluster</a> (GPU nodes for visualizing images & using software requiring a graphical user interface, or "GUI")
4. The <a href="https://www.colorado.edu/rc/resources/petalibrary" target="_blank">CURC PetaLibrary</a> (storage of O2A datasets)

__Gateways__: The computing and storage resources can be accessed through the following gateways:

1. Via the command line (Access to Blanca or Summit for batch computing, or PetaLibrary for data transfer)
2. Via the <a href="https://www.colorado.edu/rc/resources/jupyterhub" target="_blank">CURC JupyterHub</a> (Access to Blanca or Summit to run iPython notebooks)
3. Via <a href="https://www.colorado.edu/rc/resources/enginframe" target="_blank">CURC EnginFrame</a> (Access to the Visualization cluster)
4. Via <a href="https://www.globus.org" target="_blank">Globus</a> (transfer files to/from PetaLibrary or other CURC filesystems)

_See the [Quick Start Guide](#span-style-color-green-quick-start-guide-span) to access CURC resources via gateways._

## Definitions

### <a href="https://oit.colorado.edu/services/identity-access-management/identikey" target="_blank">IdentiKey</a>
_An IdentiKey consists of a CU Boulder username and an IdentiKey password. An IdentiKey is the credential that uniquely identifies you to online services and campus computing facilities so that they may grant you access._

### <a href="https://www.colorado.edu/rc/resources/summit" target="_blank">RMACC Summit</a>
_An NSF-funded supercomputer operated by CURC and freely available to CU users and affiliates._

### <a href="https://www.colorado.edu/rc/resources/blanca" target="_blank">Blanca</a>
_The CURC condo computing service "Blanca" offers researchers the opportunity to purchase and own compute nodes that will be operated as part of a shared cluster. The aggregate cluster is made available to all condo partners while maintaining priority for the owner of each node. Odor2Action owns a Blanca node for use by O2A affiliates._

### <a href="https://www.colorado.edu/rc/resources/petalibrary" target="_blank">PetaLibrary</a>
_A CURC service that enables the storage, archival, and sharing of research data. It is available at a subsidized cost to any researcher affiliated with the University of Colorado Boulder. The Odor2Action project owns a PetaLibrary allocation for use by O2A affiliates._

### <a href="https://www.globus.org" target="_blank">Globus</a>
_A web-based service that enables quick and intuitive data transfer and sharing between endpoints._

### <a href="https://docs.globus.org/faq/globus-connect-endpoints/#what_is_an_endpoint" target="_blank">Endpoint</a>
_An "endpoint" is a Globus term referring to one of the two file transfer locations – either the source or the destination – between which files can move. Once a resource (server, cluster, storage system, laptop, or other system) is defined as an endpoint, it will be available to authorized users who can transfer files to or from this endpoint._

### <a href="https://www.colorado.edu/rc/resources/enginframe" target="_blank">EnginFrame cluster</a>

_The CURC EnginFrame cluster provides a 3d-accelerated remote desktop environment on an Nvidia GPU-equipped compute node hosted by CURC. Coupled with the proprietary Desktop Cloud Visualization (DCV) VNC server, the CURC EnginFrame supports the use of common visualization applications in a typical desktop environment (e.g. Matlab, Rstudio) using only a web browser._

### <a href="https://www.colorado.edu/rc/resources/jupyterhub" target="_blank">JupyterHub</a>
_JupyterHub is a multi-user server for Jupyter (formerly known as IPython) notebooks. It provides a web service that allows you to create and share documents that contain live code, equations, visualizations and explanatory text. CURC hosts a JupyterHub environment that enables researchers to utilize CURC-hosted storage and computing resources._

# <span style="color:green">QUICK START GUIDE</span>

## Step 1: Getting a CU Identikey

___What?___ An IdentiKey consists of a CU Boulder username and associated password. The CU O2A personnel will sponsor non-CU O2A affiliates so that they can obtain an IdentiKey. 

___Why?___ An IdentiKey enables users to access CU services, including CURC resources.

___How?___ Non-CU O2A affiliates may request an IdentiKey by emailing the O2A PM [Kathryn.Cochran@colorado.edu](mailto:Kathryn.Cochran@colorado.edu) with the following information:
* Full legal name of individual to be sponsored**
* Birth date**
* Gender**
* A personal email address (CUIdM uses this email address for account claiming)

___How long will it take?___ The IdentiKey provisioning process usually takes a couple of days; please plan ahead.

_** This information is required by CU's Office of Information Technology (OIT) and is used to determine if an account already exists.  Additional information can be found on the CU OIT [Sponsored Affiliates pages](https://oit.colorado.edu/identikey-accounts/sponsored)_

## Step 2: Getting a CURC Account

___What?___ A CURC account consists of a username and password that will be identical to your IdentiKey username and password.

___Why?___ A CURC account enables access to CURC resources and also ensures you have your own user directories on CURC systems.

___How?___ Once you have obtained a CU IdentiKey, complete the following steps:

1. You will have received an official CU Email address, usually `<IdentiKey>@colorado.edu`. For example, if your IdentiKey is `jodo2020` your CU email address will be `jodo2020@colorado.edu`. Please make sure they you either 1) check this email regularly or 2) forward email from this address to your personal email address. This is important because CURC account correspondence will go to your `<IdentiKey>@colorado.edu` address. 

2. Now navigate to the [CURC accounts management portal](https://rcamp.rc.colorado.edu/accounts/account-request/create/verify/ucb). You will come to the following screen:

![](images/o2a_rcamp.png)
 
Do the following:
* enter your IdentiKey username and password where prompted.
* enter "Odor2Action" for your _Department_
* choose "Sponsored Affiliate" for your _Role_
* click on `Verify and Continue`.

On the next screen, if you are prompted about which resource you wish to access, choose "Blanca". Finish the process to submit your account request. You will receive an email to your `<IdentiKey>@colorado.edu` email address when your account has been provisioned. 

___How long will it take?___ Accounts are generally approved and provisioned within 1-2 hours during M-F business hours. After hours or weekend requests may not be provisioned until the next business day.

## Step 3: Setting up Duo 2-Factor Authentication

___What?___ In addition to your IdentiKey password, logging into CURC resources requires a "second factor" for authentication; this is similar to the text message you may receive on your phone when you enter a password to log into a bank account. CURC uses a 2-factor authentication service called "Duo". 

___Why?___ Two-factor authentication enhances the security of CURC systems by ensuring the user is you.

___How?___ You will receive a message to your `<IdentiKey>@colorado.edu` email address noting that your Duo account has been established.  Momentarily, you will receive a second email, an invitation from Duo.  Follow the instructions in the Duo invitation to install the Duo app on your phone and link your CURC account. 

_Additional information can be found in the [CURC Duo documentation](https://curc.readthedocs.io/en/latest/access/duo-2-factor-authentication.html)._

___How long will it take?___ Duo accounts are usually provisioned when your CURC account is established (Step 2 above). It will take 5 minutes or less to set up the Duo app on your smartphone and link it to your account.  

## Step 4: Accessing CURC Resources

After completing Steps 1-3 above you will be able to login to CURC systems via a variety of _gateways_ depending on the resources you wish to access. Each gateway is described below. 

### Accessing PetaLibrary (file transfer)

The O2A project has an allocation on <a href="https://www.colorado.edu/rc/resources/petalibrary" target="_blank">CURC PetaLibrary</a>, which is CURC's data storage and sharing platform. While there are numerous ways to transfer files to/from PetaLibrary, <a href="https://www.globus.org" target="_blank">Globus</a> is the recommended means of doing so. Users who prefer using command line methods for file transfers (e.g., _scp_, _sftp_ or _rsync_) may refer to the [CURC data transfer documentation](https://curc.readthedocs.io/en/latest/compute/data-transfer.html).

Globus is a web-based service that enables quick and intuitive data transfer and sharing between _endpoints_. Globus addresses deficiencies in secure copy requests by automating large data transfers, resuming failed transfers, and simplifying the implementation of high performance transfers between computing centers. An "endpoint" is a Globus term referring to one of the two file transfer locations – either the source or the destination – between which files can move. Once a resource (server, cluster, storage system, laptop, or other system) is defined as an endpoint, it will be available to authorized users who can transfer files to or from this endpoint.

#### Using Globus to Transfer Files

[Sign into Globus](https://www.globus.org/app/login) by
selecting "University of Colorado at Boulder" from the dropdown menu
and by logging in using your CU IdentiKey and password.

![](https://raw.githubusercontent.com/ResearchComputing/Research-Computing-User-Tutorials/master/File-Transfers/globus-image-1.png)

Files can easily be transferred to/from PetaLibrary or other CURC filesystems, from/to your local computer with Globus.

* _Step 1_: A Globus endpoint has already been established to connect you to CURC. You can connect to this endpoint by clicking the "Collection" field and searching for the endpoint: `CU Boulder Research Computing`. Log into the end point with your CU IdentiKey and password.

* _Step 2_: Your local computer must also have an endpoint. You can easily set up a Globus endpoint by installing [Globus Connect Personal](https://www.globus.org/globus-connect-personal) on your local machine. Once you have established your local endpoint, go back to [Globus](https://www.globus.org/app/login) in your browser and connect your local workstation endpoint on the other half of the Globus "File Manager" screen (you can search for the name of your endpoint in the "Collection" field). Now you can tranfer files between your local machine and CURC.   

![](https://raw.githubusercontent.com/ResearchComputing/Documentation/june-updates/File-Transfers/globus-image-2new.PNG)

Note that you can use the "Path" field to navigate to the O2A PetaLibrary allocation. Type `/pl/active/odor2action` in the "Path" field, and then you can use your mouse to navigate deeper into the O2A allocation if needed.

#### Sharing data with Globus Shared Endpoints
With Globus you can share files with users outside of CU who do not have CURC accounts by creating shared endpoints. You can share any file/folder that you have access to.  The user you are sharing with has to have a Globus account.

To learn how to setup a shared endpoint:
[Globus Shared Endpoint Documentation](https://docs.globus.org/how-to/share-files/)

### Accessing JupyterHub (python notebooks)

[Jupyter notebooks](https://jupyter.org/) are an excellent resource for interactive development and data analysis using _Python_, _R_, and other languages. Jupyter notebooks can contain live code, equations, visualizations, and explanatory text which provide an integrated enviornment to use, learn, and teach interactive data analysis.  

CU Research Computing (CURC) operates a [JupyterHub server](https://jupyterhub.readthedocs.org/en/latest/) that enables users to run Jupyter notebooks on Summit or Blanca for serial (single core) and shared-memory parallel (single node) workflows. The CURC JupyterHub uses the next-generation [JupyterLab](https://jupyterlab.readthedocs.io) user interface. The CURC JupyterHub runs atop of [Anaconda](http://anaconda.com).  Additional documentation on the [CURC Anaconda distribution](https://curc.readthedocs.io/en/latest/software/python.html) is available and may be a good pre-requisite for the following documentation outlining use of the CURC JupyterHub.

#### Step 1: Log  in to CURC JupyterHub

CURC JupyterHub is available at [https://jupyter.rc.colorado.edu](https://jupyter.rc.colorado.edu). To log in use your RC credentials. If you do not have an RC account, please [request an account before continuing.](https://rcamp.rc.colorado.edu/accounts/account-request/create/organization)

#### Step 2: Start a notebook server

To start a notebook server, select one of the `Blanca (12hr)` option in the *Select job profile* menu under *Spawner Options* and click *Spawn*. 

The server will take a few moments to start.  When it does, you will be taken to the Jupyter home screen, which will show the contents of your CURC `/home` directory in the left menu bar. In the main work area on the right hand side you will see the "Launcher" and any other tabs you may have open from previous sessions.

<p align="middle">
  <img src="https://raw.githubusercontent.com/ResearchComputing/Documentation/dev/docs/gateways/jupyterhub/jupyterlab1.png"/>
</p>

#### Step 3: Navigating the JupyterLab Interface

The following features are availabe in the [JupyterLab Interface](https://jupyterlab.readthedocs.io/en/stable/user/interface.html):

* _Left sidebar:_ Click on a tab to change what you see in the left menu bar.  Options include the file browser, a list of running kernels and terminals, a command palette, a notebook cell tools inspector, and a tabs list.
* _Left menu bar:_ 
  * The _file browser_ will be active when you log in. 
    * You can navigate to your other CURC directories by clicking the folder next to `/home/<username>`. Your other CURC file systems are available too: `/projects/<username>`, `/pl/active` (for users with PetaLibrary allocations), `/scratch/summit/<username>` (Summit only), and `/rc_scratch/<username>` (Blanca only).
    * To open an existing notebook, just click on the notebook name in the file browser (e.g., _mynotebook.ipynb_).
    * Above your working directory contents are buttons to add a new Launcher, create a new folder, upload files from your local computer, and refresh the working directory. 
* _Main Work Area:_ Your workspaces will be in this large area on the right hand side. Under the "Launcher" tab you can: 
  * Open a new notebook with any of the kernels listed:
      * __Python 3 (idp)__: Python3 notebook (Intel Python distribution)
      * __Bash__: BASH notebook
      * __R__: R notebook 
      * ...and any other custom kernels you add on your own _(see the [section below](#creating-your-own-custom-jupyter-kernels) on creating your own custom kernels)._
   * Open a new console (command line) for any of the kernels.
   * Open other functions; the "Terminal" function is particularly useful, as it enables you to access the command line on the Summit or Blanca node your Jupyterhub job is currently running on. 
* See Jupyter's [documentation on the JupyterLab Interface for additional information.](https://jupyterlab.readthedocs.io/en/stable/user/interface.html)

##### Tip for finding the packages available to you within a notebook

The ___Python 3___ notebook kernel has many preinstalled packages. To query a list of available packages from a python notebook, you can use the following nomenclature:

```
from pip._internal import main as pipmain 
pipmain(['freeze'])
```

If the packages you need are not available, [you can create your own custom environment and Jupyter kernel](#additional-documentation).

    
##### For users who prefer the "old school" classic Jupyter interface in favor of JupyterLab

You can access the Jupyter classic view by going to the address bar at the top of your broswer and changing "lab" to "tree" in the URL.  For, example, if your session URL is https://jupyter.rc.colorado.edu/user/janedoe/lab, you can change this to https://jupyter.rc.colorado.edu/user/janedoe/tree . 

#### Step 4: Shut down a Notebook Server

Go to the "File" menu at the top and choose "Hub Control Panel". Use the `Stop My Server` button in the `Control Panel` to shut down the Jupyter notebook server when finished (this cancels the job you are running on Blanca). You also have the option to restart a server if desired.

Alternately, you can use the `Quit` button from the Jupyter home page to shut down the Jupyter notebook server.

Using the `Logout` button will log you out of CURC JupyterHub.  It will not shut down your notebook server if one happens to be running.  

#### Additional Documentation

##### Creating your own custom Jupyter kernels

The CURC JupyterHub runs on top of the [CURC Anaconda distribution](https://curc.readthedocs.io/en/latest/software/python.html). [Anaconda](http://anaconda.com) is an open-source _python_ and _R_ distribution that uses the _conda_ package manager to easily install software and packages. Software and associated Jupyter [kernels](https://github.com/jupyter/jupyter/wiki/Jupyter-kernels) other than _python_ and _R_ can also be installed using _conda_. The following steps describe how to create your own custom Anaconda environments and associated Jupyter kernels for use on RC JupyterHub. 

Follow these steps from a terminal session. You can get a new terminal session directly from Jupyter using `New`-> `Terminal`.

###### 1.  Configure your conda settings

Follow our Anaconda documentation for [steps on configuring your conda settings via ~.condarc](https://curc.readthedocs.io/en/latest/software/python.html#configure-your-conda-settings).

###### 2. Activate the CURC Anaconda environment

```
[johndoe@shas0137 ~]$ source /curc/sw/anaconda3/latest
```

You will know that you have properly activated the environment because you should see `(base)` in front of your prompt. E.g.: 

```
(base) [johndoe@shas0137 ~]$
```

###### 3. Create a new custom environment. 

Follow our Anaconda documentation for [steps on creating your own custom conda environment](https://curc.readthedocs.io/en/latest/software/python.html#create-your-own-custom-environment).


###### 4. Activate your new environment

```
(base) [johndoe@shas0137 ~]$ conda activate mycustomenv
```

(Note: we assume here that you've named your environment _mycustomenv_; please replace _mycustomenv_ with whatever name you gave your environment!)

###### 5. Create your own custom kernel, which will enable you to use this environment in CURC Jupyterhub:

```
(mycustomenv) [johndoe@shas0137 ~]$ conda install -y ipykernel
(mycustomenv) [johndoe@shas0137 ~]$ python -m ipykernel install --user --name mycustomenv --display-name mycustomenv
```

The first command will install the ipykernel package if not installed already. The second command will create a kernel with the name _mycustomenv_ with the Jupyter display name _mycustomenv_ (note that the name and display-name are not required to match the environment name -- call them anything you want). By specifying the `--user` flag, the kernel will be in `/home/$USER/.local/share/jupyter/kernels` (a directory that is in the default __JUPYTER_PATH__) and will ensure your new kernel is available to you the next time you use CURC JupyterHub.


###### Notes:
* If you have already installed your own version of Anaconda or Miniconda, it is possible to create Jupyter kernels for your preexisting environments by following _Step 4_ above from within the active environment.  
* If you need to use custom kernels that are in a location other than `/home/$USER/.local/share/jupyter` (for example, if your research team has a group installation of Anaconda environments located in `/pl/active/<some_env>`), you can create a file in your home directory named `~/.jupyterrc` containing the following line:

```
export JUPYTER_PATH=/pl/active/<some_env>/share/jupyter
```

If you need assistance creating or installing environments or Jupyter kernels, contact us at rc-help@colorado.edu. 

###### Using Dask to spawn multi-core jobs from CURC JupyterHub

_Dask is a flexible library for parallel computing in Python. Documentation for using Dask on RC JupyterHub is forthcoming. In the meantime, if you need help integrating Dask with Slurm so that you can run multicore jobs on the CURC JupyterHub, please contact us at rc-help@colorado.edu._

#### Troubleshooting

Jupyter notebook servers spawned on RC compute resources log to `~/.jupyterhub-spawner.log`. Watching the contents of this file provides useful information regarding any problems encountered during notebook startup or execution.

#### See Also

* [CURC Anaconda distribution](https://curc.readthedocs.io/en/latest/software/python.html)
* [JupyterLab homepage](https://jupyterlab.readthedocs.io)

### Accessing EnginFrame (visualization, GUIs)

NICE EnginFrame provides a 3d-accelerated remote desktop environment
on an Nvidia GPU-equipped compute node. Coupled with the proprietary
Desktop Cloud Visualization (DCV) VNC server, the EnginFrame service
supports the use of common visualization applications in a typical
desktop environment using only a modern web browser.


#### Step 1: Request access and login to EnginFrame

Access to EnginFrame is granted on request. Request access by sending
email to [rc-help@colorado.edu](rc-help@colorado.edu).

Once access has been granted, EnginFrame is available at
[https://viz.rc.colorado.edu/](https://viz.rc.colorado.edu/).

From the welcome page, select "Views" from the available interfaces (or use [this direct link](https://viz.rc.colorado.edu/enginframe/vdi/vdi.xml)).

![](images/welcome.png)

Provide your RC login credentials at the login prompt. You will be
promted to use a second authentication factor (e.g., the Duo mobile
app) to log in.

![](images/login.png)


#### Step 2: Starting a remote desktop

After logging in, select "Remote Desktop" from the list of services in
the left sidebar. (Other custom services may be configured for you as
well.)

![](images/vdi.png)

When starting a Remote Desktop session you may customize the resources
allocated to the session and other characteristics of the dispatched
Slurm job. In most cases the defaults should be sufficient; however,
you may need to supply a Slurm account if you are associated with more
than one and you do not want to use your default account.

![](images/remote-desktop.png)

Once the session has started, a thumbnail of the running session
appears in the Sessions list. EnginFrame will attempt to open the
session automatically, but may be blocked by the browser. In that
case, simply select the session thumbnail from the list, or use the
"click here" link in the notification text.

![](images/session.png)

With the Remote Desktop session running and open, you should be able
to run standard Linux desktop applications, including 3d-accelerated
OpenGL applications.

![](images/glxgears.png)

#### Additional Resources

- [https://www.nice-software.com/products/enginframe](https://www.nice-software.com/products/enginframe)
- [https://www.nice-software.com/products/dcv](https://www.nice-software.com/products/dcv)


### Accessing the O2A Blanca node (command line, batch computing)

# <span style="color:green">OTHER TOPICS</span>

## Using Matlab on CURC

Coming Soon

# <span style="color:green">FAQ</span>

## I have a new phone and Duo isn't working

Coming Soon

## I can't access the O2A Blanca node

Coming Soon

## I can't access the O2A PetaLibrary space

Coming Soon
