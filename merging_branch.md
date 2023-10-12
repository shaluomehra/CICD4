# Merging Branches

**We only want working code on the Main branch**

We are going to be merging the dev branch with the main branch

- `git branch dev` to create the dev branch
- `git checkout dev` to change to the dev branch


### Create a new job in Jenkins that will automate this

![Screenshot 2023-10-12 104547.png](images_3%2FScreenshot%202023-10-12%20104547.png)
- Discard Olds Builds - max #3
- Link the Github Project

![Screenshot 2023-10-12 104648.png](images_3%2FScreenshot%202023-10-12%20104648.png)
- Restrict where project can be run: `sparta-ubuntu-node`

![Screenshot 2023-10-12 105001.png](images_3%2FScreenshot%202023-10-12%20105001.png)
- We want to use the **dev** branch so change the branch specifier

![Screenshot 2023-10-12 105052.png](images_3%2FScreenshot%202023-10-12%20105052.png)
- We want to add an additional behaviour: **Merge before build**
- Name of repo: origin
- Branch to merge to: main (If code is successful merge to main)

![Screenshot 2023-10-12 105236.png](images_3%2FScreenshot%202023-10-12%20105236.png)
- We want to build this job only after our test is successful

![Screenshot 2023-10-12 105348.png](images_3%2FScreenshot%202023-10-12%20105348.png)
- Include the SSH agent: tech254.pem
- To communicate with AWS

### Push to GITHUB if successful

Here we use Git Publisher, to merge the results if the test is successful

![Screenshot 2023-10-12 121105.png](images_3%2FScreenshot%202023-10-12%20121105.png)







