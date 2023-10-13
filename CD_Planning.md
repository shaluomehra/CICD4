# Steps to Create a Jenkins CI/CD Task
![screenshot.png](images_4%2Fscreenshot.png)
## Step 1  (Create a Jenkins Job)

- Open Jenkins and log in
- Create new job called 'shaluo-CD' 
-  Configure the job settings

![Screenshot 2023-10-13 131943.png](images_5%2FScreenshot%202023-10-13%20131943.png)
- Max 3 builds
- Link the Github project URL

![Screenshot 2023-10-13 132049.png](images_5%2FScreenshot%202023-10-13%20132049.png)
-Restrict the job to `sparta-ubuntu-node`

![Screenshot 2023-10-13 132149.png](images_5%2FScreenshot%202023-10-13%20132149.png)
- Link the SSH URL to the Repositories
- Private Key Attached
- This time we want to use the **main** branch as it is working code

## Step 2 (Trigger the Job)

- In the build trigger we only want 'shaluo-CD' to work if the merge is successful

![Screenshot 2023-10-13 132338.png](images_5%2FScreenshot%202023-10-13%20132338.png)
- We want to only build this project once the merge is successful
- We also want to use a webhook to Github

## Step 3 (Jenkins SSH)

![Screenshot 2023-10-13 132442.png](images_5%2FScreenshot%202023-10-13%20132442.png)
- Provide the .pem file so Jenkins can SSH into the VM

## Step 4 (Copy the app code)

- Use a build step in 'shaluo-CD' to copy the application code
- Lets first start with getting Nginx on to our Virtual Machine
```
rsync -avz -e "ssh -o StrictHostKeyChecking=no" app ubuntu@54.171.236.179:/home/ubuntu
ssh -o "StrictHostKeyChecking=no" ubuntu@54.171.236.179 <<EOF
	sudo apt-get update -y
    sudo apt-get upgrade -y
    sudo apt-get install nginx -y
    sudo systemctl restart nginx
    sudo systemctl enable nginx
EOF
```

#### Step 5 (Change the app directory)

- Change the directory to where the app is located

#### Step 6 (NPM Install)

- We need to `npm install`  (?)

#### Step 7 (Install node.js)

- We need to install node.js or use an AMI that has node instlled

#### Step 8 (Change the name)

- Add a build step to configure the name of the Sparta app to shaluo-sparta

























































