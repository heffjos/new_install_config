# new_install_config
keeps track of installation procedure for new ubuntu (16.04 and 18.04) installtions

### Ethernet (if needed)
1. Request ethernet port activation for either managed or collaborative network. Linux machines not set with a static ip address will have network access whereas ones with a static ip address will not.
2. If needed, request a static ip address from help. This is primarily done for machines on unmanaged network.
3. Request machine added to DNS from G.
4. Configure the static ip address on the machine. (Need to figure out how this is done. The network install script was not successful on an ubuntu 18.04 machine following this approach.)
5. Request RCC access from M.

### Upgrade packages
At terminal run:
1. `apt-get update`
2. `apt-get upgrade`

### Additional repositories

#### Neurodebian
1. `apt-get install neurodebian`
2. `apt-get update`

#### Chrome web browser
Use the .deb file provided by google: https://www.google.com/chrome
1. `wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb`
2. `sudo dpkg -i google-chrome-stable_current_amd64.deb`
3. The .deb file will add the official Google repository to the system. Check `/etc/apt/sources.list.d/google-chrome.list`

#### Docker




