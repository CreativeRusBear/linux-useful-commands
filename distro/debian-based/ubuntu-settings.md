# Ubuntu settings and cheatsheet

1. Hotkeys:
    * Switching between tabs: `Win + Tab`
    * Changing tab size:
        * Maximize tab on the full window size: `Win + ↑`
        * Return previously tab size: `Win + ↓`
        * Press the tab to the left side: `Win + ←`
        * Press the tab to the right side: `Win + →`
    * Opening the calendar tab: `Win + M`  
    * Creating screenshots:
        * Creating fullscreen screenshot: `PrtScr`  
        * Creating the certain tab (window) screenshot: `Alt + PrtScr`
        * Creating the certain area screenshot: `Shift + PrtScr`
        
2. Settings:
    * `Google Chrome` update settings:
    
    ```bash
    $ wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo apt-key add -
    $ sudo sh -c 'echo "deb http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google-chrome.list'
   
    $ sudo apt-get update
    $ sudo apt-get --only-upgrade install google-chrome-stable
    ```
   * Install `Node.js` v.13 and `npm`:
   
   ```bash
   $ sudo apt -y update && sudo apt -y upgrade
   
   $ curl -sL https://deb.nodesource.com/setup_13.x | sudo bash -
   
   $ sudo apt-get install -y nodejs
   ```
   
   * Install `Yarn` package manager:
   
   ```bash
   $ curl -sL https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
   $ echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
   $ sudo apt-get update && sudo apt-get install yarn
   ```
   
   * Install `screenfetch` and additional info about work with it:
   
        * Installation: 
       ```bash
       $ sudo apt install screenfetch
       ```
   
        * Work with it:
            * Run utility:
            
            ```bash
            $ screenfetch
            ```
          
            * Output info without logo:
                        
            ```bash
            $ screenfetch -n
            ```
          
            * Change color of output text:
                                  
            ```bash
            $ screenfetch -c1
            $ screenfetch -c2
            $ screenfetch -c3
            ```
          
            * Get info about work of utility:
            
            ```bash
            $ screenfetch -h
            ```
   * [`htop`](http://linux-bash.ru/menusistem/79-htop.html) installation and additional info about work with it:
        * Installation `htop`:
        
        ```bash
        $ sudo apt-get install htop
        ```   
        
        * Work with it:
            * Run utility:
                    
            ```bash
            $ htop
            ```  
            
            * Columns:
                * **PID** - process id;
                * **USER** - process owner.
                * **PRI** - current priority (affect on process time, allotted process, default value - 20; than less priority, then more time allotting on process, therefore it runs faster).
                * **NI** - priority change amount regarding PRI value (F7, F8 keys).
                * **VIRT** - general virtual memory size,that using process.
                * **DATA** - memory size, that filling data, which using process in runtime.
                * **SWAP** - memory size, that using process, but moving at swap area.
                * **RES** - the amount of resident (not swapable) memory in kilobytes.
                * **SHR** - the amount of shared program memory in kilobytes, so that memory, which can be using other applications. 
                
                * **S** - process state:
                * **S** - so named "sleep state";
                * **R** - "running state";
                * **D** - "waiting state";
                
                * **CPU%** - CPU usage as a percentage.
                * **MEM%** - memory usage by percentage.
                * **TIME+** - process time.
                * **Command** - indicates the command by which the process was started.
                
                Also next params are outputting on the screen:
                
                * **Load average** - displaying count of blocking processes in the execution queue at a certain time interval, namely 1, 5 and 15 minutes, respectively.
                Blocking process is a process, that waits resources for continue work.
                * **Uptime** - system work time.
                
            * Control:
            
                * **F1** - help desk;
                * **F2** - settings;
                * **F3** - find process;
                * **F4** - process list sorting (from more to less or from less to more);
                * **F5** - set tree view and vice versa;
                * **F6** - opens a panel with a choice of process sorting option;
                * **F7** - increase an execution priority for current process;
                * **F8** - decrease an execution priority for current process;
                * **F9** - kill process;
                * **F10** - quit from program.