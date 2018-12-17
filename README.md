# Vagrant-Ansible-Jenkins

The scope of this script is to provide a full install of Jenkins CI using vagrant in your laptop.
The name of the newly create VM will be **jenkins**

```
vagrant status
Current machine states:

jenkins                   running (virtualbox)
```

# How to use it

There are just few steps to follow

1) Be sure to have vagrant installed in your laptop, otherwise follow these instrutions to install it https://www.vagrantup.com/intro/getting-started/install.html

2) Clone the repository or download the zip file 

    `git clone https://github.com/MassimoDanieli/Vagrant-Ansible-Jenkins.git`

    *or*

    `unzip  Vagrant-Ansible-Jenkins-master.zip`

3) Go to the new directory and spin up the vagrant machine and let ansible do the work !

    `cd Vagrant-Ansible-Jenkins && vagrant up`

4) Copy the initial Jenkins admin's password from the latest ansible task
    ```
    TASK [jenkins : print init password jenkins] ***********************************
           ok: [jenkins] => {
        "result.stdout": "ed83571837eb42fbadb4548f08e12e35"
    }
    ```
    

5) Open your favorite browser and connect to   http://127.0.0.1:8080 or http://YOUR_IP:8080 
The admin username is **admin** and the password is the one shown in point 4)

6) Your Jenkins CI is now up and running: don't forget to check its documentation page https://jenkins.io/doc/

