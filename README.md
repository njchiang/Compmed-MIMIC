# Compmed-MIMIC
Code for setup and analysis of MIMIC data in the Compmed MIMIC account

Make sure to get access to PhysioNet prior to getting access to this AWS environment

# AWS Environment

## Daily operation
1. Sign in to your IAM account at https://651111875052.signin.aws.amazon.com/console
2. Switch to us-east-1

If Instance is not already running... otherwise skip to step 6

3. launch ec2 instance and ssh in: `ssh -L 9999:localhost:[JUPYTER PORT] ec2-user@[DNS NAME FROM INTERFACE]`
4. launch JupyterLab using `jupyter lab --no-browser --port=[JUPYTER PORT]`

If instance is already running...

5. Connect either using port forwarding (not configured yet) or using actual address: `ssh -NL 9999:localhost:[JUPYTER PORT] ec2-user@[DNS NAME FROM INTERFACE]`

6. Navigate to localhost:9999 on the local machine to use JupyterLab to compute 
7. MAKE SURE TO SHUT DOWN THE INSTANCE WHEN DONE TO SAVE COSTS

## EC2 Instance Setup 
Run these when setting up a new instance
1. Install miniconda `wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh`
2. Make sure conda is enabled
3. install JupyterLab `conda install -c conda-forge jupyterlab`
4. run aws configure (may want to change to default credentials)
5. create additional kernels (optional)
6. Run the "Getting Started" notebook to test the connection.

## Initial setup (already run, just for documentation)
- Launch AWS Athena Stack to piggyback off their setup. MAKE SURE TO STOP THE SAGEMAKER INSTANCE.
- make sure to set up port forwarding (Jeff to look into how to get a browser address for jupyterlab)
- Make sure account ID is associated with Physionet

# Resources
https://mimic.mit.edu/docs/gettingstarted/cloud/

https://physionet.org/content/mimiciii/1.4/

https://aws.amazon.com/blogs/big-data/perform-biomedical-informatics-without-a-database-using-mimic-iii-data-and-amazon-athena/
