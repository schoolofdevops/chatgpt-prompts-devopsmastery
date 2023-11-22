# ChatGPT Prompts for Generating Scripts and Automation Code 

Pick the relevant scripting language or tool to generate the code with best practices and relevant context provided. 

## Shell Script 

I need help generating a shell script for use case described below. While generating the script , add comments wherever necessary to help me understand the code. Incorporate best practices,  add logic to accept command line options using getopts with default block to show help with -h and --help. Ensure you follow good security practices as well to make it DevSecOps compliant. Write individual functions along with a main function block. Use control stuctures whererver necessary. Annotate variables. Ask for shell and operating system distribution before you start generating the code. Explain how to execute this script. Assume sudo is available unless explicitly mentioned otherwise. Use awk or sed as and when needed if its text processing task. 

Here is the use case : 

xxxx


## Python Script 

I need help generating a Python  script for use case described below. While generating the script , add comments wherever necessary to help me understand the code. Incorporate best practices,  add logic to accept command line options with default block to show help with -h and --help. Ensure you follow good security practices as well to make it DevSecOps compliant. Write individual functions . Use control structures  wherever necessary. Annotate variables. Use virtual environment. Write modular code. Explain how to execute this script. 
Here is the use case :


xxxx


## Dockerfile 

I need help generating a Dockerfile for the following use case. While writing the Dockerfile ask me for the language this application is written in if relevant or its a off the shelf application, base image if any, port to expose etc.  Wherever possible, generate a Multi Stage Dockerfile. Suggest to use optimized based imaged based on alpine or equivalent. Try to optimize the RUN instructions wherever possible. Try to incorprate security best practices such as creating and configuring a non root user and switching to it to launch the application with. Use build arguments wheverver possible. Add a health check to the Dockerfile. Add a default command to the Dockerfile. Add default environment variables to the Dockerfile. Add default labels to the Dockerfile. Ask me what I want to write the Dockerfile for today before you generate it. 


## Kubernetes Manifests 

I need help generating a Kubernetes Manifest for the following use case. While generating the manifest, automatically select the right resource type for the workload described e.g. Deployment, Statefulset, DaemonSet, Jobs, CronJobs etc.se StatefuleSet for stateful applications such as databases etc. Whenever you generate StatefulSet, also add the VolumeClaimTemplate configuration.  Also create a service manifest along with it. Prompt user for the type of service and port to expose, however use nodeport as a default and try to guess the service port smartly. Prompt user if they want to add PersistentVolumeClaim configuration, Ingress Rule, RBAC Policy etc. Provide a NetworkPolicy with liberal default rules which can be changed later.  While writing the pod template, add  default resource configurations with min and max values for  cpu and memory  defined by smartly guessing the default range of values based on the application or language being used. Add lables such as app, role, version to all resources.  Add any other best practices related to pod template as necessary.  Also add default configuration for rollouts in the spec. Add annotation field in the metadata to describe the change-cause .  Ask me to describe which application I want to deploy today on the kubernetes cluster in simple english language before you begin generating the code. 



## Jenkinsfile without Containers 


I need help generating a Jenkinsfile to run Continuous Integration jobs for the following use case. Use declarative pipeline syntax for better readability and ease of use. Use consistent naming conventions, indentation, and comments. Use parameters for builds to make your Jenkinsfile flexible and reusable.  Define environment variables for reusable values. Provide clear documentation within the Jenkinsfile. Use stages to group related steps together and to break down a complex pipeline into smaller, more manageable chunks.  Keep security best practices in mind and make it DevSecOps compliant. Add a post action block to print a success or a failure message when the pipeline succeeds or fails respectively.   Generate a simple CI Pipeline which has build,  test and package stages. Use parallel stages to run test stage with two stages namely unit test, and  add a placeholder stage to run in parallel. Execute the package stage conditionally only on the master branch.  Never add the logic to checkout a repository from revision control system as the Jenkinsfile will be part of the code itself and will get executed only after the code is already checked out. Add artifacts archival as part of the package stage. Assume global tools configuration is available and refer to  it in Jenkinsfile.  Remember this is not a container based application. 

Here is my use case: 

I want to create a Jenkinsfile to setup a CI Pipeline for a java application which uses springboot as the framework/language and maven as a build tool.  

## Jenkinsfile with Containers 


I am on a mission to upScale my Career by achieving Mastery on Devops Skills. I need help generating a Jenkinsfile to run Continuous Integration jobs for the following use case. Use declarative pipeline syntax for better readability and ease of use. Use consistent naming conventions, indentation, and comments.  Never add the logic to checkout a repository from revision control system as the Jenkinsfile will be part of the code itself and will get executed only after the code is already checked out.  Use parameters for builds to make your Jenkinsfile flexible and reusable.  Define environment variables for reusable values. Provide clear documentation within the Jenkinsfile. Use stages to group related steps together and to break down a complex pipeline into smaller, more manageable chunks.   Keep security best practices in mind and make it DevSecOps compliant. Add a post action block to print a success or a failure message when the pipeline succeeds or fails respectively. Assume this is a containers based application.  Generate a standard CI Pipeline which has build,  test,  image build and publish stages along with deploy to dev with compose. Also add a stage to scan the image for vulnerabilities using trivy by providing the correct command. Use a parallel stage block for test stage and define it with two stages, one to run unit tests, other to lint the Dockerfile using hadolint. Conditionally execute image build and publish stage along with deploy to dev stages only on master branch. In the notes section after the Jenkinsfile code,  provide the list of plugins should be used to make docker and docker-compose available along with link to the URL for plugin documentation. Assume Jenkins Global Credentials store has docker login credentials stored in the username and password format with id being 'dockerlogin'.  In the script block to build and publish the image, use docker.withRegistry function along with docker.build to buit the image using environment variable BUILD_NUMBER to dynamically increment the tag. Additionally, tag it with version aliased to dev while pushing the image. Assume Docker Hub as the default container registry.  




## Ansible 

I need help generating a Ansible Playbook along with relevant roles, inventory, manifests, vars and templates  for use case described as below. While generating the code , add comments wherever necessary to help me understand the code. Incorporate best practices including good security practices to make this code  DevSecOps compliant. Use data driven code with usage of variables and templates. Provide default values for the variables. Provide a sample inventory file when necessary. Create modular and reusable code.  

Here is the use case :

xxxx

## Terraform 

I need help generating a Terraform Module along with relevant manifests, resources, variables and templates  for use case described as below. While generating the code , add comments wherever necessary to help me understand the code. Incorporate best practices including good security practices to make this code  DevSecOps compliant. Use data driven code with usage of relevant modules as necessary.  Use input and output variables as well as templates as and when necessary. Provide default values for the variables.  Create modular and reusable code.   

Here is the use case :

xxxx


## Argo Rollout 

I need help generating the rollout manifest that I could use with Argo Rollouts for the following use case. While generating the code , add comments wherever necessary to help me understand the code. Incorporate best practices including good security practices to make this code  DevSecOps compliant. Use blue green rollout strategy as default. Prompt me to provide you with application name, release strategy and then ask the relevant information needed to implement that strategy.  Provide suggested code to implement automated analysis. 


## HELM Charts 


I need help generating a HELM chart for the use case described below. While generating the code , add comments wherever necessary to help me understand the code. Incorporate best practices including good security practices to make this code DevSecOps compliant. Create data drive, modular and reusable code. Define values along with templates.  Use consistent naming conventions while defining and referring the values and metadata. Define charts metadata using best practices. Keep the templates simple. Provide default values. Add dependencies as and when necessary. Choose whether to use deployment, statefulset, daemonset, cronjob , job by smartly guessing the type of microservice and its use.  Provide service, ingress, network plicy, rbac policy and persistent volume claims which can be enabled with a flag.  Provide a sample values file when necessary. Ask me for the use case before start generating the code. 

