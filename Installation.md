---
title: Installation
---
[Click here to subscribe for an email notification when a new version of CogStat is released.](https://forms.gle/vxFfuiQpG5nBZJSm9)

### Install and use CogStat on Windows

1. If you update from a previous version, uninstall the previous CogStat first (uninstall is available in the Start menu). Parallel installed versions may not work.
1. [Download the installer](https://www.cogstat.org/download.html) (.exe file), and run it.
    - The installer is not signed at the moment. Your operating system or your anti-virus package may warn you about this.
1. After the installation, CogStat is available from the Start menu.

(If you want to use CogStat in [Jupyter Notebook](Jupyter-Notebook) or if you want to use a smaller installer by adding CogStat to your existing Python installation, see the instructions in the relevant section below.)

<!---
1. Download and install your favorite Python distribution (e.g. [WinPython](https://winpython.github.io/) or [Anaconda](https://www.anaconda.com/))
    - Anaconda users should use the Anaconda prompt for the installation.
--->

### Install and use CogStat on Mac

1. [Download the disk image containing the app](https://www.cogstat.org/download.html) (.dmg image file), and mount it.
2. Copy the app file into the Applications folder as instructed to have it installed on your system, or run the Cogstat.app from the DMG directly (in this case, you won’t have CogStat available in the Applications list).
3. When opening the CogStat app, note that MacOS will remind you to be cautious about the software you downloaded from the internet. Continue with “Open”.

(If you want to use CogStat in [Jupyter Notebook](Jupyter-Notebook) or if you want to use a smaller installer by adding CogStat to your existing Python installation, see the instructions in the relevant section below.)

<!---
0. Note that these instructions may not work for older macOS versions. Most probably you need at least macOS 10.13.
1. Install some of the required packages (you may skip this part if you update your CogStat and have already run this before).
    * Open a terminal
        * Press Command+Space, type Terminal, and press the enter key.
    * Install brew
        * Type `ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"` and hit enter.
    * Install a new Python 3 and the PyQt Python module
        * Type `brew install python3` and hit enter.
        * Type `brew install pyqt5` and hit enter.
2.
    * Type `pip3 install Downloads/cogstat-version.tar.gz --user` (use the version number of your downloaded file) and hit enter.
        * This may take some time depending on the speed of your internet connection.
--->

### Install and use CogStat on Linux

At the moment we don't have a simple installer for Linux. However, Python is most probably already installed on your Linux, and it is relatively easy to install CogStat to your Python distribution. See the description in the relevant section below how to install CogStat on your system.

Also, you can add a shortcut to your menu via the menu editor of your desktop environment or anywhere else. If you need an icon, you can download it from [here](https://github.com/cogstat/cogstat/tree/master/cogstat/resources).

After installing CogStat, you'll be able to use it in [Jupyter Notebook](Jupyter-Notebook) too.
<!--
1. Install some required packages (you may skip this part if you update your CogStat, and have already run this before)
    * On a Debian- or an Ubuntu-based distribution you can use the command line:
        * `sudo apt-get install python3 python3-tk python3-pip python3-notebook python3-setuptools`
        * Alternatively, you can install these packages with any graphical package manager.
        * Some of these packages may be already on your system.
        * On other distributions the package names may differ.
-->

---

### Install CogStat in your existing Python installation for smaller installer size or to use it in Jupyter Notebook

1. [Download the CogStat python package](https://www.cogstat.org/download.html) (.tar.gz file)
2. Install it. The method may depend on your system; choose one of these:
    * Use pip: `pip3 install cogstat-version.tar.gz` (use the version number of your downloaded file)
        * On Linux, use root/admin access to install it system-wise.
    * Or Anaconda users should use the Anaconda prompt for the installation.
3. Run CogStat with the graphical user interface:
    * (New in v2.3) Type in your console: `cogstat` or type `python3 -m cogstat`
4. Or use [CogStat in Jupyter Notebook](Jupyter-Notebook).
    * After installation, CogStat is available to use in Jupyter Notebook

### Install the preview versions of CogStat

Preview versions (beta and release candidate) are our test releases before we release the final version. You can try the new features using the preview version and give us feedback about the software.

1. Go to the [Releases page](https://github.com/cogstat/cogstat/releases), and see if the latest release (the one at the top of the page) is a preview release (you can see a Pre-release label next to the version number).
    * If not, then use our latest stable release and enjoy CogStat. Otherwise:
2. From the Assets category, depending on your operating system, download the relevant .exe (for Windows), .dmg (for Mac), or .tar.gz (for Linux) file, and follow the OS-specific installation procedure as seen above.
