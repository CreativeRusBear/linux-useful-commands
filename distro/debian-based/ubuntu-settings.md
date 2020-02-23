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
   * `htop` installation and additional info about work with it:
        * Installation `htop`:
        
        ```bash
        $ sudo apt-get install htop
        ```   
        
        * Work with it:
            * Run utility:
                    
            ```bash
            $ htop
            ```  