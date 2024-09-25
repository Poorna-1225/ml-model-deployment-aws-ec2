# ml-model-deployment-aws-ec2
Create the ML model
Export it into a model using pickle

#Deployment steps:
create an aws account
create EC2 instance and configure it with all the configurations required
 selecting the os of the instance
 creating or using the exist keypair(we use this keypair to connect with the ec2 instance we created. Inshot we use it as a protection key)
 updating the inboud rules. open instance-> security-> choose security group-> add rule and save rule.
 next download putty and winscp
  winscp: WinSCP is primarily used for secure file transfers between a local computer and a remote server(ec2 instance we created)
   we need to login first. 
    login steps: hostname(we get this from ec2 instance configuration details. click ssh connect and copy the address mentioned) and enter user name(by default it will be the os we select. If not, it will be the name you mentioned) and then password would be the keypair (.pem file) we use to connect with ec2 instance created. if you are not able to upload .pem file convert it into .ppk file and upload it. and click on login.
    then transfer the files from local machine to server.

    acess the ec2 server using putty and install
      python3( sudo apt install python3)
      install all the required packages or libraries metioned in the requirements.txt file  (pip install -r requirements.txt)


    run the app.py file (python3 app.py)
    using ec2 puvlic ipv4 adderess access the url and copy paste with :8080  in browser and you can see the flask app you built.
    
      
  
