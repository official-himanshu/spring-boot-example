## Scenario:

Madhukaraphatak is a java developer developed some code which is running fine on his local and wamt you to streamline his work using devops methodologies, Your job is to create CI-CD for him so that he just have to code and push to github and rest of the things can take care itself.

## Acceptence Criteria:

1. Figure out the ways to run this project as local and on remote server.
2. Different Branching strategy should be used. (i.e. Production , testing and Development these three branches will be used. Tests will run in all the three Branches but in Production Branch test will run as well as a deploy application to production). 
3. Deploy that application to the remote instance.
4. Email notification will be generated too saying the status of the job is it successfully completed or not. (Hint: Configure Email Notification plugin)
5. Pipeline should trigger with commits in github repo by using webhook trigger.
6. Do follow all the best practice and convention at every steps/stages (i.e. Git, maven, CI-CD, plugins etc).
