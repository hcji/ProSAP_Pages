# Stable version

**Download Link:**

Windows: [ProSAP-0.99.4-Windows.zip](https://zenodo.org/record/5529497/files/ProSAP-0.99.4-Windows.zip?download=1)    
Linux: [ProSAP-0.99.4-Linux.tar.xz](https://zenodo.org/record/5529497/files/ProSAP-0.99.4-Linux.tar.xz?download=1)    
MacOS: [ProSAP-0.99.4-Mac.zip](https://zenodo.org/record/5529497/files/ProSAP-0.99.4-Mac.zip?download=1)

## Windows 
The installer version should be preferred but might require administrator permissions. 
Please follow the video of the installation at [video folder](https://github.com/hcji/ProSAP/tree/master/video).

**Note**:   
1. Since we do not pay Microsoft for certification, you might have to confirm that you want to trust 
"software from an unknown source". 
2. When installing, please do **not** change the default path, because sometimes we find it does not run correctly with customized path.  
3. We observed unknown errors happened if you have installed multiple versions of R. Uninstall all version of R and reinstall the latest version will fix the error.  
4. When running for the first time, it may need a long time to install the R package. There will be some requirements showing in the command prompt window, you should just follow the instructions.  

## Linux
Please follow the following installation steps and refer the video of the installation at [video folder](https://github.com/hcji/ProSAP/tree/master/video):   

1. Install [R](https://cran.r-project.org/)

        sudo apt-get install r-base
  
2. Install extra dependency of QT:

        sudo apt-get install libxcb-xinerama0

3. Download the tgz file and unzip to any folder and execute ProSAP.  
4. Execute the binary file:

        ./ProSAP
        
5. When running for the first time, it may need a long time to install the R package. There will be some requirements showing in the command prompt window, you should just follow the instructions.  
        
        
## MacOS
Please follow the following installation steps and refer the video of the installation at [video folder](https://github.com/hcji/ProSAP/tree/master/video): 

1. Allow software from unknown developers:  

        sudo spctl --master-disable
        
2. Install [R](https://cran.r-project.org/)
3. Download the zip file and unzip to any folder and execute ProSAP.
4. Execute the binary file:

        ./ProSAP
        
5. When running for the first time, it may need a long time to install the R package. There will be some requirements showing in the command prompt window, you should just follow the instructions.  


## MacOS with M1 chip
If you are using MacBook Pro with M1 chip, you should install [Rosetta](https://machow2.com/rosetta-mac/) first.    
Then, you should install [R](https://www.r-project.org/) of **High Sierra version** (Inter 64 based). This is because rpy2 has not support ARM64 based R yet. 
We will update if rpy2 support it in the future.  
Next, you can follow the same step 1 ~ step 5 of MacOS.  


**Note:** ProSAP has been test on Windows 7, Windows 10, Windows 11, Ubuntu 20.04 and MacOS 11.6.1. However, it does not work on Windows XP.

# Development version

## Windows or MacOS
1. Install [Anaconda](https://www.anaconda.com/)  or [Miniconda](https://docs.conda.io/en/latest/miniconda.html)   
2. Install [R](https://cran.r-project.org/)  
2. Install [Git](https://git-scm.com/downloads)  
3. Open commond line, create environment and enter with the following commands:  

        conda create -n ProSAP python=3.8
        conda activate ProSAP

**Note:** MacBook Pro with **M1** chip may need python=3.9 and make sure R version is suitable.
4. Clone the repository and enter:  

        git clone https://github.com/hcji/ProSAP.git
        cd ProSAP

5. Install dependency with the following commands:  
        
        pip install requirements.txt
        
6. Run ProSAP.py:  

        python ProSAP.py
        
7. Or, you may want to compile binary and run exe:  

        pyinstaller ProSAP.py -i ./img/ProSAP.ico --hidden-import=“sklearn.utils._weight_vector” 
        cd dist/ProSAP
        ProSAP.exe
        
## Linux
1. Most Linux distributions have included git and conda, but you may need install extra dependency of QT:  

        sudo apt-get install libxcb-xinerama0
        
2. Install [R](https://cran.r-project.org/)

        sudo apt-get install r-base
        
3. Refer the step 3 ~ step 7 of Windows or MacOS.  