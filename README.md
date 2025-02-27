# alpha

1. Login to AWS and launch an instance. 
   - Connect to the instance via SSH or PuTTY.

2. Switch to root and update the machine:
   sudo su
   yum update -y

3. Install Docker and start the Docker service:
   yum install -y docker
   service docker start

4. Create a directory and an HTML file for the application:
   mkdir html-app
   cd html-app

5. Edit index.html using nano or vim:
   nano index.html

6. Create and configure the Dockerfile:
   nano Dockerfile
   code
   FROM httpd
   COPY ./ /usr/local/apache2/htdocs


7. Build the Docker image:
   docker build -t html-app .

8. List Docker images:
   docker images

9. Run the Docker image as a container:
   docker run -itd -p 80:80 --name html-app html-app

10. List running Docker containers:
   docker ps

11. Access the application:
   - Copy the public IP of your instance and paste it in a browser to view the running application.
,
,
,
,
,
,
,
,
,
,
,
,
,
,
,
,
,
1. sudo su
2. yum update -y
3. yum install docker -y
4. service docker start
5. sudo usermod -a -G docker ec2-user
6. systemctl enable docker
7. service docker status
8. docker info
9. docker images
10. docker pull ubuntu
11. docker images
12. docker run -it -d ubuntu
13. docker ps
14. docker ps -a
15. docker exec -it <containerid> bash
16. exit
17. docker run hello-world
18. docker pull alpine
19. docker images
20. docker run -t ubuntu
21. docker images
 
.
.
.
.
.
.
.
.
.
.
.
.
# Navigate to the home directory
cd

# Check the installed Git version
git --version

# Access help for Git configuration
git help config
git config --help

# Create a new directory named "Flame" and navigate into it
mkdir YourDirectory
cd YourDirectory

#In windows go to c users folder and then open the created directory and inside that directory create an text file 
 
# Initialize an empty Git repository in the "Flame" directory
git init

# Check the status of the repository
git status

# Add the file "FlameOmkar.txt" to the staging area
git add Filename.txt

# Commit the changes with a message
git commit -m "Committing a Text file"

# Set the global GitHub username
git config --global user.username AccountName

# Add a remote repository link
git remote add origin link of repository.git

# Push changes to the remote "master" branch on GitHub
git push origin master
.
.
.
.
.
.
.
.
.
.
.
.
Steps to Set Up Jenkins Master-Slave Architecture
Install Jenkins and Java (if not already installed):

Ensure Jenkins and Java are installed on both the master and any potential slave machines.
Set Up Jenkins on the Master Machine:

Start the Jenkins server on the master machine.
Open Jenkins in a browser (default: http://localhost:8080).
Create a Folder for Jenkins Configuration:

Go to ProgramFiles > Jenkins and create a folder to store configuration files for slave setup.
Add Path in Jenkins Configuration:

Enter the path of the folder created in the "Remote Root Directory" field when configuring the slave node in Jenkins.
Assign a label to the node to help identify it (useful for job allocation).
Adjust Security Settings:

Go to Manage Jenkins > Configure Global Security.
Adjust the security settings as needed, enabling the slave machine to communicate with the Master.
Set Up Slave Node:

In Jenkins, navigate to Manage Jenkins > Manage Nodes and Clouds > New Node.
Create a new node, set the label (as created in step 4), and input the slave machine details.
Save and connect the slave to the master by starting the slave agent (this may involve a download).
Open Command Prompt:

On the slave machine, open Command Prompt in the Jenkins folder and execute any necessary commands (e.g., Java commands to run the Jenkins agent).
Create a New Job:

In Jenkins, go to New Item, name the job, and select a job type (e.g., Freestyle project).
Add the label of the slave node to ensure that this job runs on the specified node.
Add a Java File:

In the job workspace, create a Java file named Hello.java or any file relevant to your build.
Configure Node Tools:

Go to the node settings in Jenkins, select Configure, and add any necessary tools or environment settings.
Build the Project:

Run a build by selecting the Build Now option in the job.
Jenkins will dispatch the job to the slave node as per the label configuration.
Verify and Adjust Configuration (if needed):

Check the build status, logs, and results.
Make necessary adjustments to configurations based on build outcomes.
