# Compmed-MIMIC
Code for setup and analysis of MIMIC data in the Compmed MIMIC account

# AWS Environment
## Initial setup
make sure to set up port forwarding (Jeff to look into how to get a browser address for jupyterlab)

## Daily operation
1. Sign in to your IAM account at https://651111875052.signin.aws.amazon.com/console
2. Launch EC2 instance if not already connected
3. launch JupyterLab using `jupyter lab --no-browser`
4. Connect either using port forwarding or using actual address: `ssh -NL 9999:localhost:8888 ec2-user@ec2-52-24-33-54.us-west-2.compute.aws.com`
5. Use JupyterLab to compute
6. MAKE SURE TO SHUT DOWN THE INSTANCE WHEN DONE

## EC2 Instance Setup
1. Install miniconda `wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh`
2. Make sure conda is enabled
3. install JupyterLab `conda install -c conda-forge jupyterlab`
4. ...
