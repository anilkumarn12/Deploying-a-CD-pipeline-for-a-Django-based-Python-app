# Deploying a CD pipeline for a Django based Python app

# Pre-requisites:
•	Microsoft account setup
•	Azure account and subscription setup
•	Create a VM (Ubuntu 18.0.4) in Azure Cloud
•	Create Personal Access Token in Azure DevOps

Open on microsoft Azure portal
![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/a0af0208-9607-4926-8083-1aa7ae5b6435)

Click on sign in

![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/2b374c87-dd3a-468e-b1b9-17164ac62488)

I am sign in GitHub 

Click  on Virtual machine
![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/4f946ee2-becd-4165-bc33-6852bf5abb70)


Create on Virtual machine
![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/1ebb8aea-0d6f-45a4-8b61-b43c153ae82b)



copy on ssh_id
![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/94d08bd3-895c-4dfc-90e5-9e30f4203ad2)


Search on  Azure Devops organizations
![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/859c10f3-cd0f-4f24-8537-bef3db306ff0)


Click on My Azure Devops organization
![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/216d01aa-0f4d-419d-b99f-011ac8ddb3e4)


Click  on Create on organization
![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/4b64d35c-be8d-4a68-bdf2-28ce47c07f05)


Enter the organization name and which location you want create projects
![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/1031fcad-e631-4392-8403-afac9657061f)


My Azure organization created in anilkumatn0459
![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/8f323423-c083-441b-8423-f3121ce2bc16)


Go to settings select on Personal Access Token click
I am already created one Token name is Anil-token
![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/4fa86524-5b25-4991-bb64-abc139bea84b)


Go to command Prompt
![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/ff255f63-dcd6-49b2-bef8-345f0168f812)
Azure vm ssh key successfully connected


Step #1 - Create the Agent
 mkdir newagent >> cd newagent

Step #2 - Download the agent
tar zxvf vsts-agent-linux-x64-2.214.1.tar.gz
![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/f8f8d414-b73c-49f3-8e5d-d9c997b97460)
![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/7f20a079-b472-4a86-b99b-e497effcf282)


List the files in the directory after extracting.
ls -al
![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/aabe6caf-5206-45a6-971f-e2a36570e62e)

![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/6053d636-4ef0-4498-abfc-96d8a3bcdb68)
Azure pipeline was created


Accept the Team Explorer Everywhere license agreement now?
Type Y and enter
 ![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/cc0b17ea-7028-4cb4-8013-9a9e27e150ad)
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
![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/d30e40dc-defa-4a4a-b586-b399c7852f9f)


I am providing below link u can click showing on same Template is default and give the project name, select your organization and click on the create project after then automatically created in your organization showing project 
![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/0e881dd5-42aa-4887-9145-f39e9dc1b429)
https://azuredevopsdemogenerator.azurewebsites.net/environment/createproject


This is My project  created by latest_pythondjango
![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/f0481f47-c46c-4873-9c8d-99dfcec53bf7)


Repos>>Files>>app>index.html click and edit line-32 updated
![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/dc6fd677-f65c-40be-a8fc-3ac341b9228c)


Select on Pipelines>>Python-CI>>Edit
![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/af98e2dd-d4f9-4214-95a4-b104333b0f75)


Click on Tasks and Get sources>>Azure Repos Git
![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/2bf6c8ae-9661-4af3-9ec5-a66f59df0469)


Exactly enter the Python version and install on python in command prompt
![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/4460f1e2-263b-4ff8-b34c-8839c7b3e65e)

![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/7ed40a37-2d74-45f1-8ebd-9aba6085d106)


U can install in command prompt pip, pycmd, py.cleanup, pytest and Python 3.8.10
![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/26457fae-3549-489e-bd81-466e7e734dd8)


Once check the test results and display name
![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/3bf667ba-ae70-4672-805f-8ef351ec4a8d)


Archive file was which location downloaded and same path u will give after then created zip file
![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/73f8443d-56f2-4cf9-8473-25cea4e9d0c1)

![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/f53684e8-5735-44b5-aa03-eb8cfd708571)
Once check all details


![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/3122f2cf-5ac8-4876-b6f6-a140eb73ce54)

![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/9be14a18-3908-4e9e-a703-25642b536271)


All tasks updated after save and deploy
Python-CI successfully completed
![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/3bf10d8d-ac41-4fec-81b7-7f30e1215dc8)


My Pipeline 2nd job also successfully completed
![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/fb456442-db3f-418b-ae05-a113cb445a03)


Go to pipeline>>Releases>>click on Python-CD>>Edit>> go to tasks
![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/986df2c1-546c-4676-b070-2e1c4b79d508)


U can click on Azure subscription in free Trial and Inline Script once check (I am removing in inline script call text)
![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/987b3ede-d0ea-4d44-83e7-fc94fbae9831)


U can add on Azure subscription in Free Trial
App Service name u can mention in $(appservice-name)
![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/88d6c733-fdd0-48b3-9379-bab4caf35c06)


U can add on Azure subscription in Free Trial
App Service name u can mention in ($appservice-name)
![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/f8d2a631-465d-4582-b3aa-2b19100dda59)


Once check the details
![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/cee0dd89-8c10-4478-9b41-7ae4325d6602)


Particularly mention in Python version
![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/42d76112-5933-4935-90ab-32567e71f4ae)


![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/6ae86db1-7184-41c5-b11a-db4025761388)
Check on display-name and test results 


![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/6a26ed82-20c7-4fc0-8661-3ff3b88e10b5)
Next save and create release after then job is running 


Pipelines>>Releases>>Python-CD successfully completed
![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/1511c22c-55b6-404d-985a-ca893ac44e15)


Open on Microsoft azure >> click on App service
![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/bdf9e467-81ca-43f0-93cc-6c8ec02e054d)


Click on service name
![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/c8a8b35b-af31-4616-ab0f-d09176997f51)


Click on Browse 
![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/fd2503f6-d11b-4606-b8bc-9cabfbcd4c34)


![image](https://github.com/anilkumarn12/Deploying-a-CD-pipeline-for-a-Django-based-Python-app/assets/134625092/5eef65b0-bc78-4e39-add0-0c22ebab8fbd)
Azure Devops Project has been Successfully setup

I am provide canva link in this project i will give an access in every one can use
https://www.canva.com/design/DAFrZUuxjcc/qLzmMqcN22IVpryLnszJLA/edit?utm_content=DAFrZUuxjcc&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton

