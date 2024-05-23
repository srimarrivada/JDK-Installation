# **Install JDK8 on Windows**

The Java Development Kit (JDK) is a Java distribution being sponsored by Oracle Corporation. It implements the Java Language Specification and the Java Virtual Machine Specification and provides the Standard Edition of the Java Application Programming Interface (API).
JDK provides a software environment such as Java Virtual Machine (JVM), Compiler, Debugger, Performance monitoring tools and other utilities which are needed for developing Java applications and applets. JDK comes with a complete Java Runtime Environment (JRE) (also called as private runtime) which is separated from the regular JRE and has extra contents. 

Follow these steps to install JDK8 on Windows and use it. You can also go through [this PDF document](https://github.com/srimarrivada/JDK-Installation/blob/main/doc/Install%20JDK8%20on%20Windows.pdf) with more detailed steps along with screenshots.

## **Install JDK:**
1. Download Oracle JDK from [Oracle Java Downloads](https://www.oracle.com/java/technologies/downloads/) website.

2. You can download the latest version of Java from this website. The previous versions of JDK are also available for download from [Oracle Java Archive Downloads](https://www.oracle.com/java/technologies/downloads/archive/) website.

3. Since we are going to install JDK8, scroll down on [Oracle Java Downloads](https://www.oracle.com/java/technologies/downloads/) website to see the latest Java SE Development Kit8 release for Windows and download either x86 installer or x64 installer (depending on your 32-bit or 64-bit Windows operating system architecture) of `jdk*-windows*.exe` file.

4. You must accept Oracle license agreement to download JDK. Then it asks you to sign in. </br>
**Note:** You must have an Oracle account to download JDK. Create one if not already available.

5. After you enter Oracle account credentials, `jdk*-windows*.exe` file will be downloaded to your Downloads folder. You can copy that file to any other location.

6. Right click on the `.exe` file and select **Run as Administrator** option.

7. In few seconds, it opens up a **Java SE Development Kit Setup** wizard for installation. Press Next to proceed with the installation.

8. It then opens a **Custom Setup** dialog where we can choose the path for installation. By default, it tries to install to `C:\Program Files\Java\jdk-1.8` directory. Click on Change button if you wish to change the default installation directory.
  
9. In the next window, you can see the Progress of installation.
  
10. Next, it tries to install JRE to default installation path `C:\Program Files\Java\jre-1.8`. Click on Change button if you wish to change the installation folder.</br>
**Note:** It looks for a non-empty folder for JRE installation, so the folder you choose must be empty when you change the install path.

11. Next, it shows the Java installation progress.
  
12. Installation gets completed now and click on Close to close the window.

## **Configure JDK:**
After JDK is installed, the next step is to configure it by creating **JAVA_HOME** environment variable and adding its binary location to **PATH** environment variable.

1. In the Windows search bar, start typing “environment variables” and select the first match which opens up **System Properties** dialog.

2. On the **System Properties** window, press **Environment Variables** button.
   
3. On the **Environment Variables** dialog, press New under **System variables** tab.

4. In the **New System Variable** pane, enter the Variable name as `JAVA_HOME` and Variable value as `C:\Program Files\Java\jdk-1.8` where JDK was installed and then press OK. If you have chosen a different path during JDK install, then provide that path here.
  
5. Now choose **Path** variable under **System variables** and press Edit button.
  
6. Press New and enter value as `%JAVA_HOME%\bin` and press OK.

7. After Path variable is updated, press OK on “Environment Variables” window to apply changes and close the window.
 

## **Verify JDK Release:**
Open **Windows Command prompt** or **Windows PowerShell** and type the following command to verify the installed Java release.

`java -version`

It should show the java version (for example `1.8.0_411`) that was installed.

Now, you are ready to run any Java based applications or build applications using JDK.
