# Computer Setup
  - Installation Instructions for a PC
 
# Install Software: 
 - **NOTE: Create folder called Apps in C: (aka C:\Apps), install software in this folder unless otherwise noted.**

### R (new folder C:\Apps\R)
- R -https://www.r-project.org/. Download most recent or 1 version back.

- R - Supplemantary Installs:
  - Appendix D The Windows toolset:  http://cran.r-project.org/doc/manuals/R-admin.html#The-Windows-toolset
   
    - R Tools (**must for Windows**): https://cran.mtu.edu/bin/windows/Rtools/.  **Let this install where it wants!!!!**
    -  https://cran.mtu.edu/bin/windows/Rtools/Rtools.txt
 
   - Optional for creating PDF's with Rmarkdown: 
     - Install the complete version (new folder C:\Apps\MikTeX): https://miktex.org/download: 
     - instructions on how to use installer. https://tex.stackexchange.com/questions/345142/installation-issue
 
- RStudio (new folder C:\Apps\R\RStudio): search for RStudio, download your system's version.
  - 1.1.4x is a stable version, but old: https://support.rstudio.com/hc/en-us/articles/206569407-Older-Versions-of-RStudio
  - 2.x seems stable.

#### Other Software

- GitBash (new folder C:\Apps\GitBash): https://gitforwindows.org/.  Choose the base options.

- GitHub Desktop(kitty) (new folder C:\Apps\Github): https://desktop.github.com/

- DBeaver (new folder C:\Apps\DBeaver):  https://dbeaver.io/. Community Edition. Windows 64 bit (installer + JRE)

- OneDrive: Click on Icon in the bottom right hand-side, log in, close window. Got to  folder's properties, share with everyone.  This will allow programs to use access the folder such as github.

- WinSCP (new folder C:\Apps\WinSCP): https://winscp.net/eng/index.php. **Let this install where it wants!!!!**

  - Set up Connections for WinSCP:
    - bigred: use ssh credentials
    - Openstack (need pem file): need instructions

 - Jupyter Notebooks: https://jupyter.org/install
 
#### Java (new folder C:\Apps\Java): 
 
 - Oracle (**DEPRECATED**, SHOULD NOT USE) download:  https://www.oracle.com/technetwork/java/javase/downloads/index.html
   - Java JDK 8: is a stable release
   - Java JDK 13: Passed test and working with rJava!!!!!

 - OpenJKD 13 (C:\Apps\Java\openjdk-13.0.1_windows-x64_bin) (**PREFFERED**): 
   - Download: https://jdk.java.net/13/ PASSED TEST AND WORKING WITH rJava!!!!!! Preferred method over Java JDK 13
   
 - Reference/Instructions: https://cimentadaj.github.io/blog/2018-05-25-installing-rjava-on-windows-10/installing-rjava-on-windows-10/. 

### Environmental Variables: (must for PC, not sure about Mac)

> **RTools:** `R_TOOLS = C:\Rtools`

> **OpenJDK:** `JAVA_HOME = C:\\Apps\\Java\\openjdk-13.0.1_windows-x64_bin\\jdk-13.0.1`

> **GitHub:** `GIT_PAT = "Github Key"`

> ***Company Curl Certificates:*** `CURL_CA_BUNDLE = C:\\Apps\\R\\R-3.6.1\\library\\RCurl\\CurlSSL\\comapny-ca-bundle.crt`

> **JUPYTER_HOME** = `?`

### RESTART RSTUDIO, AND MAYBE COMPUTER - to load environmental variables ###

***Check Environmental Variables: Run `Sys.getenv()`, if CURL_CA_BUNDLE and JAVA_HOME exists, then skip, else run code below:***

 - `Sys.setenv(CURL_CA_BUNDLE = system.file("CurlSSL", "company-ca-bundle.crt" , package = "RCurl"))`
 - `Sys.setenv(JAVA_HOME = "C:\\Apps\\Java\\openjdk-13.0.1_windows-x64_bin\\jdk-13.0.1")`

