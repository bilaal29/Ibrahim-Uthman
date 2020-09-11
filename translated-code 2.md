#LAB: Google Cloud Fundamentals: Getting Started with Cloud Marketplace:

##OBJECTIVES: 

In this lab, you learn how to launch a solution using Cloud Marketplace.

##STEPS:

1. Use Cloud Marketplace to deploy a LAMP stack

        gcloud compute instances list --filter= "LAMP Certified by Bitnami" --tags = Launch
        gcloud compute zones list | grep us-central1

2. If a Welcome to Deployment Manager message appears, click Close to dismiss it

    Result:
        The status of the deployment appears in the console window: lampstack-1 is being deployed. When the deployment of the infrastructure is complete, the status changes to lampstack-1 has been deployed.After the software is installed, a summary of the details for the instance, including the site address, is displayed.

3. On the GCP Console, under Get started with LAMP Certified by Bitnami

    - Use the ssh command to open a command prompt on my-vm-1:

        ssh my-vm-1

    - In the just-created SSH window, to change the current working directory to /opt/bitnami, execute the following command:

        cd /opt/bitnami


4. To copy the phpinfo.php script from the installation directory to a publicly accessible location under the web server document root, execute the following command:

    sudo sh -c 'echo "<?php phpinfo(); ?>" > apache2/htdocs/phpinfo.php'


    To exit the command prompt on my-vm-1, execute this command:
    
        exit


5. Open a new browser tab.

6. Type the following URL:

    http://104.154.85.92/phpinfo.php


7. Close the phpinfo tab.


