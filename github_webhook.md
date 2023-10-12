# Creating a GitHub Webhook

### Step 1 (Create Webhook on Github)

Go on to your Github repo that you want to work with and click 'Settings' and from the left pane click 'Webhooks' <br> 

and then 'Add Webhook'

![Screenshot 2023-10-12 105727.png](images_4%2FScreenshot%202023-10-12%20105727.png)

### Step 2 (Managing our Webhook)

- Payload URL: This is the Jenkins URL with `/github-webhook/` attached to the end
- Content type: Change to `application/json`
- We want it to trigger on every push
- Make sure it's **Active**
- Click Save

![Screenshot 2023-10-12 110056.png](images_4%2FScreenshot%202023-10-12%20110056.png)

### Step 3 (Switch to Jenkins)

Simple step: Make sure to tick GitHub trigger on your job

![Screenshot 2023-10-12 110542.png](images_4%2FScreenshot%202023-10-12%20110542.png)

### Step 4 (Test to see if it works)

Have a test using GitBash, make a change to the README.md file in the app and then push it and see what happens!











