# jDX
jDX Distribution Software
Main updates
> sudo apt-get update  
> sudo apt-get install zip unzip  

# Installing Python
Update local repositories and install Python
> sudo apt update

Install support software
> sudo apt install build-essential zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev libssl-dev libreadline-dev libffi-dev wget

Download latest Python via source code
> cd /temp  
> wget https://www.python.org/ftp/python/3.7.5/Python-3.7.5.tgz  

Extract compressed files
> tar -xf Python-3.8.3.tgz  

Test & Optimize
> cd python-3.8.3  
> ./configure --enable-optimizations

# Install gdown
`gdown` is a library used for downloading large files from Google Drive that `wget` would normally not allow.
This library allows for files of up to 500MB to be downloaded from Google Drive via terminal or Python.

> pip install gdown  
> pip install --upgrade gdown

# Download XAMPP
Download XAMPP installer from Google Drive via 'gdown'
> gdown https://drive.google.com/uc?id=1l_5RK28JRL19wpT22B-DY9We3TVXnnQQ  

`Downloads "xampp-linux-x64-8.2.0-0-installer.run"`  

# Install XAMPP
Make installer executable
> sudo chmod 755 xampp-linux-x64-8.2.0-0-installer.run
    
Verify installer permissions 
> ls –l xampp-linux-x64-7.3.5.1-installer.run

`Expected output: "rwxr –xr –x 1 xampp-linux-x64-7.3.5.1-installer.run"`

Run package installation
> sudo ./xampp-linux-x64-7.3.5.1-installer.run

# Uninstalling XAMPP
Once the system is no longer needed, the final step after removing system files is to uninstall the server and its directory.
> cd /opt/lampp  
> sudo ./uninstall  
> sudo rm –r /opt/lamp  

# Installing SQL
Import the public repository GPG keys  
> wget -qO- https://packages.microsoft.com/keys/microsoft.asc | sudo tee /etc/apt/trusted.gpg.d/microsoft.asc  
Register the SQL Server Ubuntu repository  
> sudo add-apt-repository "$(wget -qO- https://packages.microsoft.com/config/ubuntu/20.04/mssql-server-2022.list)"  
Install SQL server  
> sudo apt-get update  
> sudo apt-get install -y mssql-server  
> sudo /opt/mssql/bin/mssql-conf setup  
Verify
> systemctl status mssql-server --no-pager

# Install SQL command-line tools  
> sudo apt-get update  
> sudo apt install curl  
Import the public repository GPG keys  
curl https://packages.microsoft.com/keys/microsoft.asc | sudo tee /etc/apt/trusted.gpg.d/microsoft.asc  
Register Ubuntu repository.
> curl https://packages.microsoft.com/config/ubuntu/20.04/prod.list | sudo tee /etc/apt/sources.list.d/msprod.list
Update the sources list and run the installation command with the unixODBC developer package.  
> sudo apt-get update  
> sudo apt-get install mssql-tools unixodbc-dev  
Update mssql-tools
> sudo apt-get update
> sudo apt-get install mssql-tools  

# Connect locally  
sqlcmd -S localhost -U <username> -P '<YourPassword>'
