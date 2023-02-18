# jDX
jDX Distribution Software and Server files

XAMPP:
https://sourceforge.net/projects/xampp/files/latest/download

# Install & upgrade 'gdown' to download XAMPP installer
> pip install gdown
> pip install --upgrade gdown 


Download installer via 'gdown'

> gdown https://drive.google.com/uc?id=1l_5RK28JRL19wpT22B-DY9We3TVXnnQQ
// downloads: xampp-linux-x64-8.2.0-0-installer.run


Make installer executable
`
sudo chmod 755 [package_name]
`
Confirm file permissions
`
ls –l xampp-linux-x64-7.3.5.1-installer.run
// expected output: "rwxr –xr –x 1 xampp-linux-x64-7.3.5.1-installer.run"
`

Run package installation
`
sudo ./xampp-linux-x64-7.3.5.1-installer.run
`

Uninstalling XAMPP
`
cd /opt/lampp
sudo ./uninstall
sudo rm –r /opt/lamp
`
