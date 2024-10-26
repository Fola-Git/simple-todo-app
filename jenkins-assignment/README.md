# Jenkins Project

This project shows how to use a tool called Jenkins. Jenkins is a tool that helps us automatically build and test our software projects, making it easier to manage our code and share it with others.

## Steps to Follow

### Step 1: Make Your Copy
1. Go to this link: [todo-list app](https://github.com/sanoojes/simple-todo-app).
2. Click on the button that says **Fork**. This will create a copy of the app in your own GitHub account.

### Step 2: Get Jenkins Ready
1. To get Jenkins, you can follow these easy instructions based on your computer type:
   - [For Linux computers](https://www.digitalocean.com/community/tutorial-collections/how-to-install-jenkins)
   - [For Windows computers](https://phoenixnap.com/kb/install-jenkins-on-windows)
   - [For Mac computers](https://www.jenkins.io/download/lts/macos/)
2. After you install it, open a web browser and type in `http://localhost:8080`. This is how you can see Jenkins.

### Step 3: Start a New Job
1. Click on "New Item" in Jenkins.
2. Choose "Freestyle project."
3. Name your job something related to the task, like "Build Todo List App."

### Step 4: Connect to Your Code
1. Look for a section called **Source Code Management**.
2. Choose the option that says "Git."
3. Enter the link to your copy of the to-do list app, for example:
   ```plaintext
   https://github.com/your-username/simple-todo-app.git
   ```

### Step 5: Tell Jenkins How to Build
1. **Add Build Step**: To tell Jenkins how to build your app, look for the section labelled **Build**.
2. Click on **Add build step** and select:
   - If you are using Linux, choose **Execute shell**.
   - If you are using Windows, choose **Execute Windows batch command**.
3. **Examples**:
   - **For Windows**:
     ```plaintext
     echo Building the app...
     ```
   - **For Linux**:
     ```bash
     echo "Building the app..."
     ```

**Why Are the Commands Different?**  
The commands are different as it depends on the operating system you are using. Hence, you must choose the correct type to avoid errors during the build process. 

### Step 6: Save What You Made
1. **Post-build Actions**: This will tell Jenkins what to do after building your app. This can be found below the build step section.
2. Click on **Add post-build action** and choose **Archive the artifacts**. This saves the files created during the build process. Specify what files to archive, like:
   ```plaintext
   **/*   # This will archive all files in the workspace
   ```

### Step 7: Finish and Check
1. Click on the **Save** button to keep all your settings.
2. Click on **Build Now** to let Jenkins start making your app.
3. After the build is complete, you can check the status:
   - A green dot means the build was successful.
   - A red dot means there was an error.
4. You can view logs to see detailed information, click on the build number in the **Build History** on the left side, then click on **Console Output**. This will show you what happened during the build process, including any errors or messages. The console output helps you diagnose issues and verify that your code is built correctly.

## Problems I Had
- **Java Trouble**: I needed to install Java before I could complete Jenkins installation on Windows.
- **Branch Confusion**: When I first built my app, I ran into an error because it was set to the master branch. After changing it to the **main** branch, I was able to build it successfully.
- **Getting Console Info**: I reviewed the console output, which provided valuable insights about what happened during the build. It helped me understand any errors when the build failed and confirmed a successful build when it succeeded.
  
## Check Out What I Built!
- I included some images to show:
  - My job configurations in Jenkins
  - A picture showing my app built successfully
  - A text file with the console output from a successful build
 
Feel free to check it out.
