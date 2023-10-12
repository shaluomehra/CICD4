### Steps to Create a Jenkins CI/CD Task

#### Step 1  (Create a Jenkins Job)

- Open Jenkins and log in
- Create new job called 'shaluo-CD'
- Configure the job settings

#### Step 2 (Trigger the Job)

- In the Merge job add a post-build action to trigger 'shaluo-CD'
- Configure the action to run when Merge job succeeds

#### Step 3 (Jenkins SSH)

- Set up an SSH access for Jenkins to your VM instance
- Make sure Jenkins has the right SSH key to access the instance

#### Step 4 (Copy the app code)

- Use a build step in 'shaluo-CD' to copy the application code 

#### Step 5 (Change the app directory)

- Change the directory to where the app is located

#### Step 6 (NPM Install)

- We need to `npm install`  (?)

#### Step 7 (Install node.js)

- We need to install node.js or use an AMI that has node instlled

#### Step 8 (Change the name)

- Add a build step to configure the name of the Sparta app to shaluo-sparta

























































