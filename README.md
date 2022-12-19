# AWS-Capstone-project-2-Hoasting-website-useing-ec2


# Overview of Steps:
                  1.Create a ec2 Amazon linux instance.
                  2.1.Create a s3 bucket

# Create a ec2 instance
    . In the AWS Management Console, navigate to ec2 → Select Amazon linux → create instance
   
   ![image](https://user-images.githubusercontent.com/110183786/208365136-2a57500d-2b1f-4e87-a50e-d934f7a279da.png)
   
# Create a S3 bucket
   . In the AWS Management Console, navigate to S3bucket → Select bucket → create bucket

   ![image](https://user-images.githubusercontent.com/110183786/208365992-5d4995ed-361b-4310-a0d7-1364888fc40a.png)


   . In the AWS Management Console, navigate to S3bucket → Select bucket → add the required files for website
   
   ![image](https://user-images.githubusercontent.com/110183786/208366710-1f0236b1-f49a-4c88-af5c-04706bc7c5bf.png)
  
   . Ssh the created ec2 instance using terminal
    
        cd ./downloads/
        
        ssh -i ./proj.pem ec2-user@3.89.109.149
        
        
   ![image](https://user-images.githubusercontent.com/110183786/208374149-1b68eb6c-90dd-4a6e-bf43-acda24fba5a5.png)
   
   . Enter the below commends
      
          sudo su
          
          yum update -y
          
          yum install httpd -y
          
    
    
   ![image](https://user-images.githubusercontent.com/110183786/208375011-a5f39f83-66e5-45ad-85d8-9fbf229c2433.png)

           cd /var/www/html
           
           wget [s3://websitedec123/demoweb (3).zip](https://webdec123.s3.amazonaws.com/demoweb3.zip)
           
           
   ![image](https://user-images.githubusercontent.com/110183786/208379243-26cd72b0-de46-4083-a72a-eba01820edd4.png)
   
   
           unzip name.zip
           
           
   ![image](https://user-images.githubusercontent.com/110183786/208379538-24861089-3e6a-4dea-a175-f644936ac33f.png)
   
           mv demoweb/* .
           
   ![image](https://user-images.githubusercontent.com/110183786/208380334-32ebc98e-6208-402b-8476-1966ae644b55.png)

           service httpd start
           
   ![image](https://user-images.githubusercontent.com/110183786/208381634-ff516158-d5e7-407d-8fea-052908a137fe.png)
   
   # End result:
   
      
   ![image](https://user-images.githubusercontent.com/110183786/208382148-202a4d1a-0433-4e17-9835-3b46b5cfce82.png)
        
   ![image](https://user-images.githubusercontent.com/110183786/208382664-44135353-2cd9-4dc9-a176-03d21a5b7dcd.png)
        
   ![image](https://user-images.githubusercontent.com/110183786/208382726-cdd9b524-f4c5-4a1c-bebc-1d60efe0aa78.png)





          
   
    
    
    
   

   

   




