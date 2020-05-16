# ConfigServerProperties
Step -I : Create New Repository for storing Application properties file on Git i.e. "ConfigServerProperties"
Step -II: Go to the any Drive and create directory with name "ConfigServerProperties"  like E:\WORKSPACE\SpringCloudConfigServerExample\ConfigServerProperties
          -Create three properties file and store on git. Use Following command to store files on git.
          -Open Git Bash on above mensioned location.
          GANESH@LAPTOP-B7D2A8DM MINGW64 /e/WORKSPACE/SpringCloudConfigServerExample/ConfigServerProperties $ git init
              Initialized empty Git repository in E:/WORKSPACE/SpringCloudConfigServerExample/ConfigServerProperties/.git/

          GANESH@LAPTOP-B7D2A8DM MINGW64 /e/WORKSPACE/SpringCloudConfigServerExample/ConfigServerProperties (master) $ git status
              On branch master
              No commits yet
              Untracked files:
              (use "git add <file>..." to include in what will be committed)
              limits-service-dev.properties
              limits-service-qa.properties
              limits-service.properties

              nothing added to commit but untracked files present (use "git add" to track)

          GANESH@LAPTOP-B7D2A8DM MINGW64 /e/WORKSPACE/SpringCloudConfigServerExample/ConfigServerProperties (master) $ git add .
              warning: LF will be replaced by CRLF in limits-service-dev.properties.
              The file will have its original line endings in your working directory
              warning: LF will be replaced by CRLF in limits-service-qa.properties.
              The file will have its original line endings in your working directory
              warning: LF will be replaced by CRLF in limits-service.properties.
              The file will have its original line endings in your working directory

          GANESH@LAPTOP-B7D2A8DM MINGW64 /e/WORKSPACE/SpringCloudConfigServerExample/ConfigServerProperties (master) $ git commit -m "First Commit"
              [master (root-commit) 159181f] First Commit
              2 files changed, 4 insertions(+)
              create mode 100644 limits-service-dev.properties
              create mode 100644 limits-service-qa.properties
              create mode 100644 limits-service.properties

          
          GANESH@LAPTOP-B7D2A8DM MINGW64 /e/WORKSPACE/SpringCloudConfigServerExample/ConfigServerProperties (master)$ git remote add origin https://github.com/gdmedage/ConfigServerProperties.git

          GANESH@LAPTOP-B7D2A8DM MINGW64 /e/WORKSPACE/SpringCloudConfigServerExample/ConfigServerProperties (master)$ git push -u origin master
              Enumerating objects: 4, done.
              Counting objects: 100% (4/4), done.
              Delta compression using up to 8 threads
              Compressing objects: 100% (4/4), done.
              Writing objects: 100% (4/4), 334 bytes | 334.00 KiB/s, done.
              Total 4 (delta 0), reused 0 (delta 0)
              To https://github.com/gdmedage/ConfigServerProperties.git
               * [new branch]      master -> master
              Branch 'master' set up to track remote branch 'master' from 'origin'.

          GANESH@LAPTOP-B7D2A8DM MINGW64 /e/WORKSPACE/SpringCloudConfigServerExample/ConfigServerProperties (master)
              $ git status
              On branch master
              Your branch is up to date with 'origin/master'.
Step-III : You can Link Local repo in eclipse Project by Following way:
           -Right click on project-->Build path-->Config Build path-->Under Java Build Path-->Select Source Tab-->Click on Link Source.
           -Provide Path of Local Git Repository i.e. E:\WORKSPACE\SpringCloudConfigServerExample\ConfigServerProperties
           -As we select Path,name will be selected automatically.
          
          
Step-IV : Set the following Properties in application.properties file of Config server to establish link between config server and git
            spring.cloud.config.server.git.uri=file:///E:/WORKSPACE/SpringCloudConfigServerExample/ConfigServerProperties
            
Step-V : If you dont want to use Local Git Repository or dont want to link Local Git Repository with eclipse, And want establish link between Config Server & Remote Git Repository then use Following property in application.properties File.
          spring.cloud.config.server.git.uri=https://github.com/gdmedage/ConfigServerProperties.git
