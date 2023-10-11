# Linking Jenkins to Github

## Create a new key

First we need to create a new Private/Public keys, we have a markdown on this I will link it here: https://github.com/shaluomehra/GitHub_SSH

We want to assign this key to the repo we want to use on Jenkins, so in this case this would be the sparta app repo, click on 'Settings' <br>

Then click 'Deploy keys' and then 'Add deploy key' 

![Screenshot 2023-10-11 143456.png](images_2%2FScreenshot%202023-10-11%20143456.png)

Copy and paste your public key here and tick the little box so you can write to it too and then click 'Save'

## Move over to Jenkins

Create a new job on Jenkins

![Screenshot 2023-10-11 164006.png](images_2%2FScreenshot%202023-10-11%20164006.png)
- Click GitHub project
- Paste in the HTTPS format of your GitHub Repo
- `https://github.com/shaluomehra/sparta_test_app.git/`

Scroll down to **Office 365 Connector**

![Screenshot 2023-10-11 164237.png](images_2%2FScreenshot%202023-10-11%20164237.png)
- Click the last box
- Copy this: `sparta-ubuntu-node`

Scroll down to **Source Code Management**

![Screenshot 2023-10-11 164432.png](images_2%2FScreenshot%202023-10-11%20164432.png)
- Copy and paste your SSH form of your repo in the Repo URL
- Select your private SSH key
- Change the branch to main

Scroll down to **Build Triggers**

![Screenshot 2023-10-11 164714.png](images_2%2FScreenshot%202023-10-11%20164714.png)
- Select Github hook trigger

**This is so we can create a Webhook from our Github**

Finally click **Save** and everything should be good to go!

















