# jDX
jDX Distribution Software

# Install 'gdown'
'gdown' is a library used for downloading large files from Google Drive that wget would normally not allow.
This library allows for files of up to 500MB to be downloaded from Google Drive via terminal or Python.

> pip install gdown  
> pip install --upgrade gdown

# Download XAMPP
Download XAMPP installer from Google Drive via 'gdown'
> gdown https://drive.google.com/uc?id=1l_5RK28JRL19wpT22B-DY9We3TVXnnQQ  
> `Downloads "xampp-linux-x64-8.2.0-0-installer.run"`  

# Install XAMPP
Make installer executable
> sudo chmod 755 xampp-linux-x64-8.2.0-0-installer.run  
Verify file permissions
> ls –l xampp-linux-x64-7.3.5.1-installer.run
> `// Expected output: "rwxr –xr –x 1 xampp-linux-x64-7.3.5.1-installer.run"`
