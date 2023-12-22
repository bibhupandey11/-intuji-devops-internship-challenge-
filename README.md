# -intuji-devops-internship-challenge-
Step 1 
Creating VM 
Downloading the Virtual box for VM
Downloaded ubuntu iso file.
Created a virtual box with Ram and disk space.
Step 2 
Installed ubuntu in storage in virtual box
Step 3
Installing docker
#First, update your existing list of packages:
Sudo apt update

#install a prerequisite packages which let apt use packages over HTTPS:
sudo apt install apt-transport-https ca-certificates curl software-properties-common

# Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl gnupg
sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
sudo chmod a+r /etc/apt/keyrings/docker.gpg

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
Step 3 
Github clone repository 
Github cloned repository was created from the terminal in ubuntu.
Sudo apt install git was used at first.
Git clone “repo url was used “ for the cloning process.
Step 4
Docker File creation
1.Docker installation was done 
2.Set up Docker's apt repository.
3.Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl gnupg
sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
sudo chmod a+r /etc/apt/keyrings/docker.gpg
# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
#Install the Docker packages.
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
#Creating DockerFile
The code was scripted in the visual studio. The already created docker file was brought up and done the running in visual studio. The hello world docker file was created.
Sudo docker build. -t test
Sudo docker run -p 80:80 test
The apache was shown in the browser.
Step 5 
Docker compose file creation
Chmod +x ~/.docker/cli-plugins/docker-compose
Docker compose version
Sudo Docker compose up
These were the command used for docker compose 
To pull docker file 
docker pull bibhu77/test

Step 6 
Jenkins setup 
Setup the Jenkins directly in the ubuntu 
Install java 
sudo apt update
sudo apt install openjdk-8-jdk -y
sudo apt install openjdk-11-jdk -y

importing the GPG key
curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo tee /usr/share/keyrings/jenkins-keyring.asc > /dev/null

Jenkins software repository to the source list and provide the authentication key
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] https://pkg.jenkins.io/debian-stable binary/ | sudo tee /etc/apt/sources.list.d/jenkins.list > /dev/null

Install Jenkins by running:
sudo apt install jenkins -y
#Open port 8080
http://localhost:8080
#Configuration of Jenkins 
Installed necessary plugins and followed the manual 

1. Clicked on New on the Jenkins dashboard.
2. Entered a name for your project 
3. Snter your GitHub repository URL.
4. Build Triggers tab was opened and choosed the git hook trigger
5. opened executed shell
6. used the command “docker build . -t test”
7.Save and project was run.
8.The error occurred in the build timeline 
9.Most of the error were solved though the last one through the docker “ sudo “ part was not solved.


