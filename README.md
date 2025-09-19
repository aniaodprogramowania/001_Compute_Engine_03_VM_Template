<p align="center">
  Google Cloud Create Simple GCP GCE VM Instance from Template
</p>

## Step-01: Introduction
1. Create an Instance Template
2. Create VM from Instance Template
3. Use **CREATE SIMILAR** option to create a clone of instance template

## Step-02: Create the Instance Template
- Go to Compute Engine -> Virtual Machines -> Instance Templates -> Create Instance Template -> Provide required details
- **Name:** my-first-instance-template
- **Location:** Regional
- **Region:** Any
- **Machine Configuration:** 
  - **Series:** E2
  - **Machine Type:** e2-micro
- **Firewall**
  - Allow HTTP Traffic
- **Advanced Options**
    - **Automation:**
      - **Startup Script:** Copy paste content from `wgrywka.sh` file
- Click on **Create**

## Step-03: Create the VM Instance using Instance Template
- **Slower-Option:** Go to Compute Engine -> VM Instances -> Create Instance -> New VM instance from template -> my-first-instance-template -> Click on Continue 
- **Faster-Option:** Go to Compute Engine -> Instance Templates -> my-first-instance-template -> Create VM
- **Name:** vm-from-my-first-instance-template
- Verify that all other configurations are loaded from the Instance Template.
- Click on **Create**

## Step-04: Verify the setup by accessing the web server pages through the VM’s External IP address.
- If needed, establish an SSH connection to the VM and verify the web server configuration directly.
```t
# Access Webserver Pages
http://<external-ip-of-vm>
```

## Step-05: Delete the VM
- In the Cloud Console, navigate to VM Instances → my-first-instance-template → Delete.
