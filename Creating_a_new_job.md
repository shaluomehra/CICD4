# Creating a job in Jenkins

Log into Jenkins and click 'New Item' or 'New Job'

![Screenshot 2023-10-11 120330.png](images%2FScreenshot%202023-10-11%20120330.png)

You will be taken to this page, create a name using **best practice** and click 'Freestyle project'

![Screenshot 2023-10-11 121246.png](images%2FScreenshot%202023-10-11%20121246.png)

We're going to create a simple task for Jenkins to see what user we are (Ubuntu, Linux etc.)

![Screenshot 2023-10-11 121502.png](images%2FScreenshot%202023-10-11%20121502.png)
- Description is not necessary, but will give a good indicator
- **Click Discard old builds** and keep at a max of 3 as this may crash our Jenkins platform

Scroll to the bottom and under 'Build' click 'Add Build step' and then click the 3rd option 'Execute Shell'

![Screenshot 2023-10-11 121726.png](images%2FScreenshot%202023-10-11%20121726.png)
- Using these commands we can see what OS we are using

Click Save and now you want to run your job, so click 'Build Now'

![Screenshot 2023-10-11 122002.png](images%2FScreenshot%202023-10-11%20122002.png)

Once it's done, click on your job and navigate to the left pane and open the 'Console Output'

![Screenshot 2023-10-11 122118.png](images%2FScreenshot%202023-10-11%20122118.png)

We can see it ran successfully and we can see out output: 

![Screenshot 2023-10-11 122220.png](images%2FScreenshot%202023-10-11%20122220.png)

## Running another iteration after job success

We have created a second job using the steps above which will show us the date using command `date -u`

![Screenshot 2023-10-11 122428.png](images%2FScreenshot%202023-10-11%20122428.png)

Now to run this job right after our first job we can configure our first job and add a 'Post-Build Action'

![Screenshot 2023-10-11 122554.png](images%2FScreenshot%202023-10-11%20122554.png)
- This will trigger if the first job is successful

Now lets run this and see what happens:

![Screenshot 2023-10-11 122702.png](images%2FScreenshot%202023-10-11%20122702.png)
- At the bottom you can see it says 'Triggering a new build of shaluo-second-job'
- Clicking on it:
![Screenshot 2023-10-11 122807.png](images%2FScreenshot%202023-10-11%20122807.png)
- We can see it ran successfully
























