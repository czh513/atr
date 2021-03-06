Nov 03 2014 | linux | Kelly Chan
# Linux Commands

### nano

- `nano file_name`: open/create a file
- `nano -w /etc/fstab`: no auto switch lines
- `ctrl+O`: save
- `ctrl+C`: cancel
- `ctrl+X`: exit

### chmod

    chmod [who] [opt] [mode] file_name
    
    who:
    - u: author
    - g: group users
    - o: others
    - a: all users
    
    
    opt: operations
    - +: add
    - -: cancel
    - =: grant
    
    mode:
    - r: read
    - w: write
    - x: execute
    
    ex. chmod g+rw a.txt


### apt-get

- install packages: `sudo apt-get install xxx`
- install python packages: `sudo aptitude install python-package-name`


### pip

    Install Easy Install
    $ sudo apt-get install python-setuptools python-dev build-essential 
    Install pip
    $ sudo easy_install pip 
    Install virtualenv
    $ sudo pip install --upgrade virtualenv 
    
    sudo pip install mysql-python
    
    apt-get install mysql-server
    
    
### passwd

    sudo passwd root
    
    # enter the root
    su
    
    
### managing files

- `sudo rm -rf folder_name`: delete the folder with all files
- `sudo rm file_name`: delete a file
- `sudo rmdir folder_name`: delete an empty folder
- `sudo mkdir folder_name`: create a new folder


### packages

- `sudo apt-get install package_name`: install a package
- `sudo apt-get autoremove package_name`: remove a package

