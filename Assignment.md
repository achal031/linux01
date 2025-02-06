# Account Setup
- In  the first step, I'd create an Microsoft Azure account using email address that university provoded me.

- Then I got  to know about the cloud and it's importance. 

- Additionally, I explored student benefits  and open an student account and Azure give me **$100** worth of credits that I can use to purchase any pachage within the environment.


# Create Virtual Machine
- I created virtual machine where I have to work later on this course.

- Then I select Marketplace from **Ubuntu Server 24.04 LTS gen 2 Server** published by Canonical. 

- I named my machine **"lab-robotics"**.

- I choose B series version 2 which is **Standard_B2ls_v2**.

- Later, I create a new resource group for the machine and subnet to place the machine in.

# Link my HAMK email to my GitHub account

- I create a new repository named **"linux"** for the assignment.

- Then I add my HAMK email as a secondary mail for version control.

![mail](img/ass1.png)


# Assignment 3: User Management and File System Access


## Step 1:
- First of all I create two users named **tupu** and **lupu**.
- I userd sudo and adduser command for that.

        sudo adduser tupu

## Step 2:
- Then I create lupu user using useradd command.
.

## Step 3: 
- Furthermore, I create the hupu system user with the login shell set to **/bin/false** file.

       sudo useradd --system --shell /bin/false hupu


## Step 4: 
- Then I use **visudo** to edit the sudoers file

        sudo visudo

- Then add the following lines for both users:

        tupu ALL=(ALL:ALL) ALL
        lupu ALL=(ALL:ALL) ALL

- There is another method as well but I present here only the only but i run both.

## Step 5:
- I create directory in **/opt/projekti** and add both users

        sudo mkdir /opt/projekti

- Then crete a group called projekti and assign both tupu and lupu into the group and the commands are:

        sudo groupadd projekti
        sudo usermod -aG projekti tupu
        sudo usermod -aG projekti lupu

- And give ownership to projekti group.

        sudo chown :projekti /opt/projekti

- And **set permission** so that tupu and lupu can access the file in all three formate like read, write and execute files.

        sudo chmod 770 /opt/projekti

- The following command ensures that any new files created within the /opt/projekti directory inherit the group ownership of projekti, maintaining the desired permissions.

        sudo chmod g+s /opt/projekti

## Output:

        drwxrws--- 2 root projekti 4096 Jan 30 14:19 /opt/projekti

![screenshot](img/image.png)


# Assignment 4 - Markdown and git 

## Step 1:
- Create a README.md file in VS code.

## Step 2:
- Fill the information with the help of markdown language.
- This include titles, lists, subtitle, examples of bold, italic, links, code block, table and inserting images.

## Step 3:
- Save this file.

## Step 4:
- Open command prompt and connect to the AZURE account with the help of personal key.
- make directory named markdown_linux_harjoitus:

                mkdir markdown_linux_harjoitus

- Go to the created directory with the command:

                cd markdown_linux_assingment

- Create a new empty file named README.md with the command:

                touch README.md

-  Check that the file was created successfully with the command:

                ll

- Open README.md file in a text editor, for example, using a nano editor:

                nano README.md

- Add the existing Markdown content to the file and save the changes.

## Step 5: Git version control
- Initialize a new Git repository in the directory with markdown_linux_assingment command:

                git init

- Add README.md file to the Git repository with the command:

                git add README.md

- Make your first commit with the command:

                git commit -m "Initial commit: Added README.md with Markdown and Linux instructions"

- Finally, these command in linux helps my first commit:)

- Following screenshot contains all the commands:

![git version control](img/image.png)
11111qqq
#### Thank You




