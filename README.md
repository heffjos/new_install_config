# new_install_config
keeps track of installation procedure for new ubuntu (20.04) installtions

### Ethernet (if needed)
1. Request ethernet port activation for either managed or collaborative network. Linux machines not set with a static ip address will have network access whereas ones not with a static ip address will not.
2. If needed, request a static ip address from help. This is primarily done for machines on unmanaged network.
3. Request machine added to DNS from G.
4. Configure the static ip address on the machine. This is done with a file in /etc/netplan.
5. Request RCC access from M.

### Upgrade packages
At terminal run:
1. `apt-get update`
2. `apt-get upgrade`
3. `apt-get install vim`

### Additional repositories

#### Neurodebian
There are instructions how to do this on the neurodebian website.

#### Chrome web browser
Use the .deb file provided by google: https://www.google.com/chrome
1. `wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb`
2. `sudo dpkg -i google-chrome-stable_current_amd64.deb`
3. The .deb file will add the official Google repository to the system. Check `/etc/apt/sources.list.d/google-chrome.list`

#### Docker
Follow this website: https://docs.docker.com/engine/install/ubuntu/

#### R
* Follow this website: https://cran.r-project.org/bin/linux/ubuntu/fullREADME.html
* Install the c2d4u ppa. This makes installing r packages so much easier.

#### Afni
Follow the installation instructions: https://afni.nimh.nih.gov/pub/dist/doc/htmldoc/background_install/install_instructs/steps_linux_ubuntu20.html
* Use option `-bindir ABIN` to set AFNI binary directory to ABIN
* `mkdir ${ABIN}/system_config` and the system afnirc file to this directory
* copy/create `afnirc` to `${ABIN}/system_config`
* add `export AFNI_SYSTEM_AFNIRC=/opt/afni/system_config/afnirc` to /etc/bash.bashrc
  * The config sets the path for the atlases and plugins. These are needed for afni to load them.

#### FSL
Follow the installation instructions: https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/FslInstallation/Linux
* Set the correct installation location. FSL creates symbolic links for some binaries so they will not be updated if the FSL folder is moved.

#### ANTS
Use guide to build it from source: https://github.com/ANTsX/ANTs/wiki/Compiling-ANTs-on-Linux-and-Mac-OS
* Install ccmake with `sudo apt-get install cmake-curses-gui`

#### Freesurfer
Install instructions are on this website: https://surfer.nmr.mgh.harvard.edu/fswiki//FS7_linux

#### Workbench
Download from this website: https://www.humanconnectome.org/software/get-connectome-workbench
