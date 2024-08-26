# PuTTY

## About PuTTY


This document contains information about PuTTY, including its functionality and key applications.

### What is PuTTY?

PuTTY is a free, open-source terminal emulator. It allows remote access to servers and network assets using protocols such as SSH, RLogin, and Telnet. Additionally, PuTTY employs several security measures to encrypt data during connections between systems.

### Functionality

It functions as a secure connection client, providing an adjustable interface. With simple commands, users can send and modify files, debug, install applications, restart the system, and execute numerous other tasks from one server to another.

### Applicability

-  Access computers and network assets remotely.
-   Facilitate secure communications between servers, even over public networks.
-   Compress extensive data during transfers to optimize the connection without impacting software performance.

## How to install PuTTY

This tutorial provides a guide on how to download and install PuTTY on your computer.

1.  Visit putty.org.
2.  Click on **Download PuTTY**.
3.  Select the version compatible with your system (32-bit or 64-bit).
4.  Choose the destination folder for the PuTTY installer and press **Save**.

Once the download is complete, proceed with the following steps:

1.  Open the PuTTY installer located in the saved folder.
2.  Click **Next** to continue with the installation.
3.  Choose the destination folder and click **Next** again.
4.  Press **Install**.
5.  Complete the installation by clicking **Finish**.


## How to move files on Windows via SSH using PuTTY

In this article, you’ll find a step-by-step guide on how to transfer files between Windows servers using the SSH protocol with PuTTY.

>⚠️ **Important** <br>
>If you haven't installed PuTTY yet, access [How to install PuTTY](https://fakewebsiteportfolio.com) tutorial.

### Step 1: Set up OpenSSH on Windows

To establish a successful connection using PuTTY, OpenSSH must be configured on the target server.

1.  Open the **Start** menu, then go to **Settings > System > Optional Features**.
2.  Check if OpenSSH is already listed. If not, click on **Add a feature** at the top of the screen.
3.  Find **OpenSSH Client** and **OpenSSH Server**, then select **Install**.
4.  Open the **Start** menu and go to **Services**.
5.  Double-click on **OpenSSH SSH Server**.
6.  On the **General** tab, set the **Startup type** to **Automatic**.
7.  Click **OK**.

You can also install OpenSSH using PowerShell 5.1 or later. For more information, access the document on [How to install OpenSSH on Windows using PowerShell](https://fakewebsiteportfolio.com).

### Step 2: Open a session in PuTTY

 1. On the source server, open PuTTY under the **Session** screen and fill in the following information:
a. **Host Name**: enter the IP address of the target server (you can find the IP address under **Settings > Network & Internet > Wi-Fi > Properties**, in the **IPv4 Address** line).
b. **Connection type**: select **SSH**.
c. **Saved Sessions**: specify a name for the target server.
 2. To save the settings, click **Save**. To establish the connection, click **Open**.
 3. The terminal window will appear, and you'll see a first-time access message on the screen. Press **Accept** to proceed with the connection.
 4. Login credentials will be required. Use the login and password associated with the Microsoft account on the target server.

Now both servers are linked, and you're able to execute commands remotely.

### Step 3: Execute the command to move files

To move files within a Windows server, execute the `move` command followed by the original file path and the destination path. For example: `move C:\Users\username\Documents\file.txt C:\Users\username\Destination`

To confirm a successful transfer, the screen will display the message **"1 file(s) moved"**.

This command can also be used to rename a file. To do so, specify the same destination path as the original, but change the filename to the desired one. For example: `move C:\Users\username\Documents\file.txt C:\Users\username\Documents\newfile.txt`

>❕ **Info** <br>
If the file name contains spaces, enclose both paths in quotes. For example: `move "C:\Users\username\Documents\file example.txt" "C:\Users\username\Destination"`

If you want to perform other remote actions using PuTTY, access [PuTTY commands](https://fakewebsiteportfolio.com).


## Reference for Session 

In this article, you will find information about the Session screen, which is the primary screen in PuTTY. This screen contains essential settings for establishing connections between servers.

>❕ **Info** <br>
For additional explanations about the screen, click on the **?** icon located in the upper-right corner. A question mark will appear next to the mouse cursor, indicating that the help mode has been enabled. Once enabled, clicking on any field will open a window displaying information about it.

#### Basic options for your PuTTY session

| **Item** | **Description** | 
:--- | :--- 
| **Host Name (or IP address)** | Name or IP address of the target server. |
| **Port** | Automatically filled in when selecting a connection type. |
| **Connection type** | The type of protocol to choose. |


#### Load, save or delete a stored session

-   **Saved Sessions**: field where you name the target server.
-   **Load**: button to load the selected server.
-   **Save**: button to save the name and pre-filled information about the target server.
-   **Delete**: button to delete the selected server.

#### Close window on exit

-   **Always**: enabling this option will close the terminal window after each session.
-   **Never**: enabling this option keeps the terminal window open but inactive after each session.
-   **Only on clean exit**: enabling this option will close the terminal window if the session ends naturally. If the session ends due to a connection issue, the terminal window will remain open.
