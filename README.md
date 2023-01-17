# xampp-installation-in-ubuntu


# xampp-installation-in-ubuntu

Installing XAMPP on Ubuntu 22.04
Please follow the following steps to download, install and configure XAMPP on your system:

Step 1: Download the installation package
The first step is to download the XAMPP package for Linux from the official Apache Friends website:

https://www.apachefriends.org/index.html

Download Xampp

Xampp for Linux

Click on the XAMPP for Linux option after which you will be prompted to Run the package or Save it to your system. We recommend downloading the package by clicking the Save File option. After which, your downloaded file will be saved to the Downloads folder by default.


Step 2: Make the installation package executable
We will install the package through the Ubuntu command line, The Terminal. In order to open the Terminal, either use the Dash or the Ctrl+Alt+T shortcut. After the Terminal is open, you need to move to your Downloads folder to access the file.

Move to the Downloads folder by using the following command:

$ cd /home/[username]/Downloads
$ ls -l xampp-linux-*-installer.run(package name)

The installation package you downloaded needs to be made executable before it can be used further. Run the following command for this purpose:

$ chmod 755 [package name]
Example:

$ chmod 755 xampp-linux-*-installer.run
Make XAMPP installer executable

Now the install package is in an executable form.

Step 3: Confirm execute permission
It is important to verify if the package can be executed by the current user. The execute permission can be checked through the following command:

$ ls -l [package name]
Example:


$ ls -l xampp-linux-x64-8.1.12-0-installer.run
The -rwxr output shows that the file can be executed by the user whose name is also mentioned in the output.

Step 4: Launch the Setup Wizard
As a privileged root user, run the following command in order to launch the graphical setup wizard.

$ sudo ./[package name]
Example:

sudo ./xampp-linux-x64-8.1.12-0-installer.run
This will launch the Setup wizard that will direct you with the rest of the installation procedure.

Step 5: Work through the graphical setup wizard
Now that the Setup Wizard for XAMPP by Bitnami is launched as follows, click the Next button to start the installation process:

Start XAMPP installer

The following dialog lets you choose XAMPP components that you want to install.

Choose which XAMPP components to be installed

Keep the default settings intact and then click Next. The following dialog will inform you about the location where XAMPP will be installed.

Select installation directory

Click Next to begin the installation process:

XAMPP ready to install

Installing XAMPP

When the installation is complete, click the Next button. The following dialog indicates the completion of the installation process.

Setup completed

If you do not want to Launch XAMPP at this moment, uncheck the Launch XAMPP option. Also, click Finish to close the Setup dialog.

Step 6: Launch XAMPP through the Terminal
In order to launch XAMPP through your Ubuntu Terminal, enter the following command as root:

$ sudo /opt/lampp/lampp start
XAMPP launch from command line

And the XAMPP control panel shows up.

Launch XAMPP

This output shows that XAMPP is started and already running. Please note that you need to manually start XAMPP each time you restart your system.

If you get the following output after starting XAMPP, it means that Net Tools are not installed on your system:

Possible errors when starting XAMPP

In order to install Net Tools, run the following command as root:

$ sudo apt install net-tools
Installing net tools

After the installation of Net Tools, you will be successfully able to launch and use XAMPP.

XAMPP launch from command line

Step 7: Verify Installation
After you have installed XAMPP on your Ubuntu system, it is good practice to verify the installation. To do so, enter the following URL in your Firefox browser:

http://localhost
The following webpage verifies that XAMPP is successfully installed and running on your system:

XAMPP Apache start page

You can also verify the installation of phpMyAdmin in a similar manner by entering the following URL in your browser:

http://localhost/phpmyadmin
The following webpage verifies that phpMyAdmin is successfully installed and running on your system:

PHPMyAdmin

Stop XAMPP Server
Use the following command to stop the XAMPP server from command line:

$ sudo /opt/lampp/lampp start
The result is:

Stop XAMPP

Uninstall XAMPP
It is also important to learn how to completely uninstall and remove XAMPP from your Ubuntu system if you ever need to do so.

Open your Ubuntu Terminal and move to the directory where XAMPP is installed. That is:

$ cd /opt/lampp
The next step is to run the uninstall program you will find in the lampp folder through the following command:

$ sudo ./uninstall
The following dialog will appear asking you if you want to uninstall XAMPP and all of its modules:

$ sudo ./uninstall
Provide the password then press <enter> if being asked for the sudo password. The system will ask for your confirmation before proceeding. Type Y then hit enter to confirm your selection.

Uninstall xampp

After some time, the Uninstallation completed information will be displayed in the output to confirm the uninstallation process.

Uninstall progresss

Uninstall process finished

Finally, you can remove the directory using:

$ sudo rm -r /opt/lampp
Remove application directory

Now, XAMPP and all its modules are uninstalled from your system. You can also delete the downloaded install package if you want.

In this tutorial, you have learned a step-by-step installation process for XAMPP on your Ubuntu System. From downloading the install package, running it, and then verifying the installation, you have walked through the entire procedure with us. We have also provided enough information about uninstalling XAMPP if you ever need to do that.



For making the shortcut gui 

open notepad 

#!/usr/bin/env xdg-open
[Desktop Entry]
Name=XAMPP GUI
Type=Application
Exec=sh -c "pkexec env DISPLAY=$DISPLAY XAUTHORITY=$XAUTHORITY sudo /opt/lampp/manager-linux-x64.run"
Terminal=false
Icon=/opt/lampp/htdocs/favicon.ico
Terminal=false


SAVE THIS  file with name Xampp.desktop

press right click on icon at give peermission to launch 

