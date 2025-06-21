# this is the readme file of github actions take home assignment

in this assignment we have to containerize an application and deply it on ec2

first i created the files and also wrote a docker file as instructed in the assignment

![image](https://github.com/user-attachments/assets/e3895e60-2414-4c06-b1d4-663c467b157b)

i also pushed the code in github.

after that i launched the ec2 instance with the required congigurations setting up all the resources like vpc, subnet, internet gateway, etc.

![image](https://github.com/user-attachments/assets/c37fc769-93a9-48e2-9140-c124b03feaf3)

after this step i SSHed into the ec2 instance using the key pair that I created and installed docker there.

![image](https://github.com/user-attachments/assets/a1631ebb-fa33-44b2-a51d-935743f0e802)
![image](https://github.com/user-attachments/assets/6bc64424-579a-4d9d-8030-7fbf3dac66ae)
![image](https://github.com/user-attachments/assets/f4b10f05-f18e-4cfd-93df-9e6166d464b4)

and after that i wrote the CICD yaml file on github in actions. I also edited the file provied in assignment as i have deployed code in master instead of main.

![image](https://github.com/user-attachments/assets/80575dd9-7545-4588-835e-0b0af4160eb7)

and also added 3 repository secrets that are EC2_HOST, EC2_USERNAME and EC2_SSH_KEY

![Screenshot 2025-06-21 152057](https://github.com/user-attachments/assets/30211006-f32e-4883-94f1-14968f5a227e)
![image](https://github.com/user-attachments/assets/5889de83-97bf-45b8-afde-b29703062800)

after this i ran the pipeline and it ran successfully.

![image](https://github.com/user-attachments/assets/d6b455d7-1a27-4edc-bd54-c94e1ca4b969)

![image](https://github.com/user-attachments/assets/65a01bf9-f1c6-49bf-9d09-46ddf39ad998)

for the next step i checked the docker ps command in ec2 instance and i can see the image there.
I also checked the output using curl http://localhost:3000 in it.

![image](https://github.com/user-attachments/assets/56d6f465-9014-499f-8dae-630364cf9cb5)

i also checked the result in browser using http://<my-ec2-ip-address>:3000

![Screenshot 2025-06-21 165504](https://github.com/user-attachments/assets/98f26375-5f92-413e-903e-4d46c2d15929)

after that i have made sure that all the resources are delted which i created in aws.

![image](https://github.com/user-attachments/assets/5418912d-6495-4ea1-b227-bab4c9d2063c)
![image](https://github.com/user-attachments/assets/6d88506d-0bb8-4b99-99b4-b128ab5c8041)
![image](https://github.com/user-attachments/assets/5d2640d2-280c-41f9-bf0a-4844d8ca4456)
![image](https://github.com/user-attachments/assets/c8ed0849-f26a-4502-9a87-75051597b1f8)
