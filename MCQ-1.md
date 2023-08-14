# MCQ on Linux, Git, Docker and Jenkins

1. Which of the following statements about the chmod , chown , chgrp , and chdir commands is true?
   a) chmod changes the owner of a file or directory, while chown modifies the group associated with it.
   b) chgrp is used to change the current working directory, while chdir alters file permissions.
   c) chmod alters file or directory permissions, chown changes the owner, chgrp modifies the group, and chdir changes the current working directory.
   d) chdir changes the owner of a file, while chgrp is used to switch directories.

2. In a typical file permission string -rwxr-xr-- , what does the first - represent?
   a) Read permission
   b) Write permission
   c) Execute permission
   d) Type of the file

3. Which of the following is a valid field in the /etc/passwd file?
   a) Password hash
   b) Last login time
   c) Home directory
   d) User's email address

4. Which command can be used to monitor real-time system resource usage?
   a) top
   b) ps
   c) lsof
   d) netstat

5. You want to run a Linux command inside an existing Docker container. Which command would you use?
   a) docker exec
   b) docker run
   c) docker ps il
   d) docker commit

6. Which command ensures that a specific service starts automatically at system boot?
   a) systemctl enable
   b) systemctl start
   c) systemctl boot
   d) systemd enable

7. What is the primary function of the Docker Daemon?
   a) To build Docker images
   b) To push images to Docker Hub
   c) To manage Docker containers, images, networks, and volumes
   d) To provide a user interface for Docker

8. Which of the following best describes the primary objective of adopting DevOps practices?
   a) Solely accelerating software releases.
   b) Maintaining distinct responsibilities between development and operations teams.
   c) Enhancing collaboration between teams, leading to swifter and more reliable software delivery.
   d) Prioritizing only new feature development, overlooking infrastructure needs.

9. Which symbol is used in a cron job definition to represent every instance (e.g., every hour, every day)?
    a) *
    b) ?
    c) !
    d) #

10. You have files in your repository you don't want Git to ever track them. What should you be doing to avoid ever tracking them?
    a) Commit them and then use git rm.
    b) Add them to .gitignore.
    c) Use the git untrack command.
    d) Move them out of the repository directory.

11. Which of the following commands will create a new branch and immediately switch to it in Git?
    a) git branch [branch-name]
    b) git checkout -b [branch-name]
    c) git checkout [branch-name]
    d) git merge [branch-name]

12. Which of the following sequences best represents a typical workflow in Git?
    a) git clone, git add, git commit, git push
    b) git pull, git commit, git add, git push
    c) git commit, git add, git clone, git push
    d) git clone, git pull, git commit, git add

13. If you want to save your changes without committing them, then continue working later, which commands would you use?
    a) git stash, git stash apply
    b) git save, git load
    c) git push, git pull
    d) git commit, git checkout

14. You've just pushed a commit to the remote repository and realized there's an error in it. Which sequence of commands would you typically use to undo the last commit and create a new commit that undoes the changes, while keeping the history intact?
    a) git reset HEAD^, git push --force
    b) git undo, git push
    c) git revert HEAD, git push
    d) git delete HEAD, git push

15. You've just joined a new project and want to understand the history of commits. Which command would you use to see a list of all commits?
    a) git show
    b) git log
    c) git history
    d) git list-commits

16. In Git, what is the meaning of the "staging area"?
    a) A temporary area where commits are stored before they are pushed to the remote repository.
    b) The area where files are stored after they have been cloned from a remote repository.
    c) An intermediate area where changes are organized and prepared before being committed to the repository.
    d) The location where Git stores metadata and object files for the repository.

17. Which of the following statements best describes the relationship between Git and GitHub?
    a) Git and GitHub are the same thing; they both are version control systems used to track changes in code.
    b) GitHub is a proprietary software, while Git is an open-source version control system. They are used for the same purpose, but GitHub has a more user-friendly interface.
    c) Git is a distributed version control system that allows developers to track changes in their code, while GitHub is a cloud-based platform that uses Git for version control and provides collaboration features like bug tracking, feature requests, and task management for projects.
    d) GitHub is an advanced version of Git, built upon Git's foundation, and is used primarily by large corporations for enterprise-level projects.

18. Which of the following commands only downloads new data from a remote repository but doesn't integrate any new data into your working files?
    a) git pull
    b) git clone
    c) git fetch
    d) git merge

19. You are troubleshooting a microservices application deployed using Docker. One of the services, named "payment-service", seems to be failing, and you suspect an issue with its recent transactions. To investigate the issue further, you decide to check the logs of the running container associated with this service. Which of the following Docker commands would you use to retrieve the logs of "payment-service"?
    a) docker logs payment-service
    b) docker inspect payment-service
    c) docker ps | grep payment-service
    d) docker view payment-service

20. What is the primary difference between a Docker image and a Docker container?
    a) An image is a running instance, while a container is a static file.
    b) An image is a blueprint, while a container is a running instance of that blueprint.
    c) Images and containers are the same thing in Docker.
    d) An image is used for data storage, while a container is used for execution.

21. What is the primary purpose of the Docker Compose tool?
    a) To build Docker images
    b) To define and run multi-container Docker applications
    c) To push images to Docker Hub
    d) To monitor running Docker containers

22. Which of the following is NOT a benefit of using Docker?
    a) Lightweight virtualization
    b) Application isolation
    c) Automatic backup of data
    d) Consistent environments

23. Which command is used to view detailed information about a specific container?
    a) docker view
    b) docker details
    c) docker inspect
    d) docker show

24. Which of the following is a best practice when creating Docker images?
    a) Make images as large as possible
    b) Include all possible tools for debugging
    c) Minimize the number of layers in the image
    d) Use a different base image for each application

25. You are working on a DevOps team and are tasked with setting up a Docker container for a new application. However, you've been instructed to only create the container without starting it immediately, as another team member will be configuring some settings before the container's first run. Which Docker command would you use to achieve this?
    a) docker start <image-name>
    b) docker run -d <image-name>
    c) docker create <image-name>
    d) docker build <image-name>

26. Which Dockerfile instruction is used to define variables that users can pass at build-time?
    a) ENV
    b) ARG
    c) VAR
    d) SET

27. Which command can be used to identify the status of a Docker container?
    a) docker status
    b) docker info
    c) docker ps -a
    d) docker inspect

28. Which of the following is the default network driver for a Docker container?
    a) bridge
    b) host
    c) overlay
    d) none

29. You're troubleshooting a Docker container that's failing to start. The logs indicate an issue with mounting a volume. Which of the following commands would provide the most detailed information about the specific volume configuration?
    a) docker volume ls
    b) docker inspect <volume_name>
    c) docker volume info <volume_name>
    d) docker ps -a

30. If you want to copy files from your Docker container to your host, which command would you use?
    a) docker cp
    b) docker copy
    c) docker export
    d) docker clone

# Here are the correct answers for the questions:

1. chmod alters file or directory permissions, chown changes the owner, chgrp modifies the group, and chdir changes the current working directory.
2. Home directory
3. Password hash
4. top
5. docker exec
6. systemctl enable
7. To manage Docker containers, images, networks, and volumes
8. Enhancing collaboration between teams, leading to swifter and more reliable software delivery.
9. *
10. Add them to .gitignore.
11. git checkout -b [branch-name]
12. git clone, git add, git commit, git push
13. git stash, git stash apply
14. git revert HEAD, git push
15. git log
16. An intermediate area where changes are organized and prepared before being committed to the repository.
17. Git is a distributed version control system that allows developers to track changes in their code, while GitHub is a cloud-based platform that uses Git for version control and provides collaboration features.
18. git fetch
19. docker logs payment-service
20. An image is a blueprint, while a container is a running instance of that blueprint.
21. To define and run multi-container Docker applications
22. Automatic backup of data
23. docker inspect
24. Minimize the number of layers in the image
25. docker create <image-name>
26. ARG
27. docker ps -a
28. bridge
29. docker inspect <volume_name>
30. docker cp
    
