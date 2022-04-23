# SplunkDockerSink
A Splunk Test Environment with Everything
3 SH 3 IDX 1 Deployer 1 CM 1 DeploymentServer 1HF 4UF

1. You will need docker and docker-compose installed on the system with the docker runtime active "sudo systemctl start docker"

2. Create a directory for the project "mkdir SplunkDocker"

3. Add the default.yml and docker-compose.yml to the directory 

4. Finally run "sudo docker-compose up"

This should fill your screen with the log of it downloading the newest Splunk versions. Assinging them Splunk roles (SH,CM,IDX,UF,HF, and etc.) along with creating a network for them to communicat through. (This seems to be broken on MAC when last tested around 2021. As always Linux is better!!)

You can run docker-compose as dettached to not see the logs or lose a terminal to it. I like the logs and just open another terminal to do anything else needed. 

I do get failures and retries at the end of the log. I haven't fully researched the issue but they don't seem to affect how I use this for testing.

5. Run "sudo docker ps" to check the status of all containers (healthy vs unhealthy) once healthy they should be good to go. This can take some time as a lot of things are happening in the background. While testing in ESXi I have a minimal Ubuntu Server running 8 CPUs with 16 GBs of RAM and it took around 20min for a clean bill of health. Sometimes Ubuntu did fail, Arch does the best so far and only took 7min to start with no failures. (EndevorOS if you don't want to install Arch).

With "sudo docker ps" you can find a Search Head (sh) and log into that IP with port 8000

Have fun and make sure you break something while you are there!!!!!!!


--------------------Helpful Links-----------------------------------------

Splunk Docker Examples
https://splunk.github.io/docker-splunk/EXAMPLES.html

Splunk Docker Test Scenarios
https://github.com/splunk/docker-splunk/tree/develop/test_scenarios
