## Unveiling the Cloud Giants: A Deep Dive into Performance Analysis of Three Leading Cloud Service Providers (AMAZON WEB SERVICE, GOOGLE CLOUD PLATFORM AND MICROSOFT AZURE)

## Prerequisites

1. Create a specific Virtual Machine
   a) Create an account with the required Cloud Service Providers
   b) Select the required instances with required configurations used and download the
   PuTTY .ppk format private key
   c) Deploy the virtual machine and wait till the deployment is successfull(it can take some time)
   `CAUTION`: some of the virtual machines may require you to pay

## Installation of PuTTY

PuTTY is needed to to SSH into the virtual machine through the host machine
You can download it according to the operating systems as follows:

`For Windows`

https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html

`For Macos`

```
brew install putty
```

### Implementation

1. After creating the instances, then next step is to SSH into the specific virtual machine which can be done using PuTTY which is an excellent SSH client
   For `Mac` on the command line or in scripts, you can use the following commands.

```
puttygen privatekey.ppk -O private-openssh -o privatekey.pem
```

Make sure permissions on the private key file are set properly. It should only be readable by the user that owns it.

```
chmod go-rw privatekey.pem
```

You can now use the key for logins from scripts and command line with:

```
ssh -i privatekey.pem user@hostname
```

2. Now you would be inside the virtual machine, `git clone` this repository after that and run the server using following commands:

```
cd "Folder Name"
```

```
npm i
```

```
node server.js
```

This will start the server at port 4000

3. Go into the Shell files folder and run any of them using the following commands:
   `Prereq:` Ddd the public IP address of the virtual machine in the shell file you want to run

```
cd shellFiles
```

```
bash "name of any of the files"
```

This will establish the connection with the nodejs server that we just deployed in the above step

### Results

Every Cloud service provider has its own Cloud Monitoring system
look at the graphs after the connection is established and requests are made
Following is an example of how the graphs might look like
![alt text](https://www.appoptics.com/-/media/solarwinds/appoptics/product-screenshots/ao-aws-ec2.ashx?rev=9c56d2dd535045dc90442a359d4e6e44)
