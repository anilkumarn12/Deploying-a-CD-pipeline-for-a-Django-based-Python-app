# Deploying-a-CD-pipeline-for-a-Django-based-Python-app

Pre-requisites:
•	Microsoft account setup
•	Azure account and subscription setup
•	Create a VM (Ubuntu 18.0.4) in Azure Cloud
•	Create Personal Access Token in Azure DevOps

Open on microsoft Azure portal
 
Click on sign in
 
I am sign in GitHub 


Click  on Virtual machine
 






Create on Virtual machine
 



Copy on ssh key id :  ssh -i myazurevm_key.pe azureuser@40.121.2.75
 




Search on  Azure Devops organizations
 


Click on My Azure Devops organization
 

Click  on Create on organization
 

Enter the organization name and which location you want create projects
 







My Azure organization created in anilkumatn0459
 




Go to settings select on Personal Access Token click
I am already created one Token name is Anil-token
 



Go to command Prompt
 
Azure vm ssh key successfully connected

Step #1 - Create the Agent
 mkdir newagent >> cd newagent

Step #2 - Download the agent
tar zxvf vsts-agent-linux-x64-2.214.1.tar.gz
 
 

List the files in the directory after extracting.
ls -al
 


 
Azure pipeline was created
Accept the Team Explorer Everywhere license agreement now?
Type Y and enter
 
Step #3:
Enter server URL >
https://dev.azure.com/yourorganization
Step #4:
Enter authentication type (press enter for PAT) >>PAT
Step #5:
Enter personal access token_id
Step #6:
Enter Agent pool
Give some name
Step #7:
Enter Agent name --> newagent
Step #8:
Enter work folder > enter
that's it agent is successfully configured.
Configure the Agent to run as a Service
Sudo ./svc.sh install
Execute now to run as a service
./run.sh

 
This is my agent  name is newagent was also online
 

I am providing below link u can click showing on same Template is default and give the project name, select your organization and click on the create project after then automatically created in your organization showing project 
 
https://azuredevopsdemogenerator.azurewebsites.net/environment/createproject





This is My project  created by latest_pythondjango
 

Repos>>Files>>app>index.html click and edit line-32 updated
 





Select on Pipelines>>Python-CI>>Edit

 	

Click on Tasks and Get sources>>Azure Repos Git
 





Exactly enter the Python version and install on python in command prompt
 


 

U can install in command prompt pip, pycmd, py.cleanup, pytest and Python 3.8.10
 


Once check the test results and display name
 




Archive file was which location downloaded and same path u will give after then created zip file
 




 
Once check all details
 



 





All tasks updated after save and deploy
Python-CI successfully completed
 



My Pipeline 2nd job also successfully completed
 






Go to pipeline>>Releases>>click on Python-CD>>Edit>> go to tasks
 














U can click on Azure subscription in free Trial and Inline Script once check (I am removing in inline script call text)
 

U can add on Azure subscription in Free Trial
App Service name u can mention in $(appservice-name)
 



U can add on Azure subscription in Free Trial
App Service name u can mention in ($appservice-name)
 


Once check the detailes
 





Particularly mention in Python version
 


 
Check on display-name and test results 
 
Next save and create release after then job is running 

Pipelines>>Releases>>Python-CD successfully completed
 





Open on Microsoft azure >> click on App service
 

Click on service name
 





Click on Browse 
 


 
Azure Devops Project has been Successfully setup









































