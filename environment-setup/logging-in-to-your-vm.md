# Logging in to your VM

To utilize your compute, you need to log in to the cluster using an SSH connection (Secure Shell). You must have shared your SSH public key with the Build AI team prior to onboarding for this to work as expected (see [onboarding.md](../onboarding.md "mention") for more info).&#x20;

Connect either via a terminal or connect the filesystem directly to VS code.

#### **Terminal**

1. Open a Terminal window.
2. Connect to the cluster using the username and node BuildAI shared with you:

```bash
$ ssh <username>@<hostname>
```

3. If this is your first time connecting, you will be asked ‘Are you sure you want to continue connecting (yes/no)?’ You can answer ‘yes’.
4. You should be connected to a Build AI GPU!

#### **VS Code**

1. Open a VS Code window.
2.  In the search bar at the top, connect to the repote host by typing ">" and selecting `remote-ssh`\
    \


    <figure><img src="../.gitbook/assets/Screenshot 2024-05-25 at 2.05.09 PM (1).png" alt=""><figcaption></figcaption></figure>

    <figure><img src="../.gitbook/assets/Screenshot 2024-05-25 at 2.05.22 PM.png" alt=""><figcaption></figcaption></figure>
3. Select ‘+ Add New SSH Host…’
4. Enter `<username>@<hostname>`. Press ‘Enter’. Select the SSH Config file to add it to.
5. Repeat step 2. This time, select the node you just added from the list of hosts.
6. Enter your password when prompted.
7. VS Code will now open a window on the remote node. You can open/edit files and run them through a terminal.

Now you have access to the Build AI GPUs!
