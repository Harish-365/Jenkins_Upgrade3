# Hello World Plugin Demo
Build a simple "Hello, World" plugin using a template.


# Install Java and Maven 
-- Java is Already Installed


## Install Maven
Download Maven Tar from https://maven.apache.org/download.cgi
Unzip tar - tar -xvzf <file_name>
move to /opt -- mv apache-maven****** /opt/


# Add the following lines to the user profile file (.profile).
M2_HOME='/opt/apache-maven-******' /opt/apache-maven-3.9.4
PATH="$M2_HOME/bin:$PATH"
export PATH

Relaunch the terminal or execute source .profile to apply the changes.
Execute mvn -version command


# Create a local folder for the source code:
mkdir -p hello-world
cd hello-world


# Create a plugin from the Jenkins templates:
mvn -U archetype:generate -Dfilter="io.jenkins.archetypes:"

**This Maven command is used to generate a Jenkins plugin project using an archetype. Let’s break it down:
Command Breakdown
mvn -U archetype:generate -Dfilter="io.jenkins.archetypes:"
- mvn → Runs Maven.
- -U → Forces an update of the local repository to get the latest archetypes.
- archetype:generate → Generates a new project from an archetype.
- -Dfilter="io.jenkins.archetypes:" → Filters available Jenkins archetypes to choose from.
What Does This Do?
- It lists Jenkins plugin archetypes available in Maven.
- You can select an archetype to create a plugin skeleton for Jenkins development.**


mvn verify
mvn package

Move .hpi file from targets to Jenkins Plugin Directory
Retstart the Jenkins Service

LogIn Jenkins and follow below steps -

- New freestyle job
- Add "Hello World" build step
- Run, check console
