# SplunkDockerSink
A Splunk Test Environment with Everything
3 SH 3 IDX 1 Deployer 1 CM 1 DeploymentServer 1HF 4UF

You will need docker and docker-compose installed on the system with the docker runtime active "sudo systemctl start docker"

Create a directory for the project "mkdir SplunkDocker"

Add the default.yml and docker-compose.yml to the directory 

Finally run "sudo docker-compose up"

This should fill your screen with the log of it downloading the newest Splunk versions. Assinging them Splunk roles (SH,CM,IDX,UF,HF, and etc.) along with creating a network for them to communicat through. (This seems to be broken on MAC when last tested around 2021. As always Linux is better!!)

You can run docker-compose as dettached to not see the logs or lose a terminal to it. I like the logs and just open another terminal to do anything else needed. 
