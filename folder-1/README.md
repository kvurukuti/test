
# BQaaF Automation

A brief description of what this project does and how shell scripting helps us achieve our goals.

We will perform two automation tasks for this project.

1. Create/Update custom roles in multiple GCP-Projects Individually by reading project Id's from the csv file and attaching that Created custom roles to the Single serviceAccount.

2. Establishing a logsink and attaching it to a dataset that already exists in destination project to route the logs. This is what we'll perform across several GCP-Projects. by reading each project ID from the CSV file individually.


### Uploading automation script files to the gcloud shell using browser.

 1. login to the GCP console and open the cloudshell in the browser.
 2. Upload the automation folder in to the shell as show in the below screenshots.
 


![App Screenshot](https://user-images.githubusercontent.com/96725131/228324346-faf7e5ed-8c24-440e-bb8d-f04681f2d0fe.PNG)

![App Screenshot](https://user-images.githubusercontent.com/96725131/228323388-90b7d038-ea2c-47e0-93ee-29c88f53b295.PNG)

![App Screenshot](https://user-images.githubusercontent.com/96725131/228324358-4b277794-840e-4e94-84dc-ff7ef6a24835.PNG)

3. Now we have uploaded 5 files to the gcloud shell which required to run the scripts as shown in the above screenshots.
### Steps for Creating/Updating roles and attaching to serviceAccount, And Creating logsink and attach to the destination dataset in another project.

- Required files to run the script.

    1. role.yaml
    2. input.csv
    3. adding-roles.sh
    4. logsink.sh

## Running shellscript for Creating/Updating custom roles and attaching to the serviceAccount

Command to run shellscript - make sure that you should be at automation directory in gcloud shell as shown in the below screenshot

![App Screenshot](https://user-images.githubusercontent.com/96725131/228330455-fa55319a-2b99-438e-9ff9-99e9fe756a57.PNG)

Command to be run for granting executing permission to the script files in the gcloud shell.
```bash
  chmod +x adding-roles.sh logsink.sh
```
Command to run the shell script for creating/updating roles
```bash
  ./adding-roles.sh
```
Command to run the shell script for creating logsink and to attach datasets
```bash
  ./logsink.sh
```

