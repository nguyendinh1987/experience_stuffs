Step 1: Install the dependencies required to build the Python package.  
  > sudo apt install build-essential zlib1g-dev \
  > libncurses5-dev libgdbm-dev libnss3-dev \
  > libssl-dev libreadline-dev libffi-dev curl software-properties-common
Step 2: Download the version tar package and extract it  
  > wget https://www.python.org/ftp/python/3.9.0/Python-3.9.0.tar.xz
  > tar -xf Python-3.9.0.tar.xz 
Step 3: Move to the extracted folder and run configuration  
  > cd Python-3.9.0
  > /configure
Step 4: Install Python 3.9 alongside your current Python installation (if any)
  > sudo make altinstall
Step 5: Verify your installation
  > python3.9 --version
Step 6: Make the installed python as the default version in the system (Optional):  
  - Using symbolic link mapping the installed python executive file to the default command. Syntax of the command creating symbolic link: ln -s path/to/executable_file path/to/default_command
  - Using alias: create an alias in ~/.bashrc file. For example, ```alias python3='/usr/bin/python3.9'```
Refs: 
1. https://opensource.com/article/20/4/install-python-linux 
2. https://stackoverflow.com/questions/60824700/how-can-i-install-python-3-9-on-a-linux-ubuntu-terminal 
