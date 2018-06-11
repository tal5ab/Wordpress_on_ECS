## OPS terraform / ansible / packer / docker test

###The Excersie

For this exercise, I would like you use tools like Terraform, Packer and Ansible. The goal is to setup a wordpress container on an ECS cluster.


I would like you use Packer with the Ansible provisioner to create a "ready to use" wordpress image that will use a rds database. The goal is not to use a fork but to do it by yourself. We are interested in the how and the result. 

You can use AWS free tier usage for that, don't waste money.


I would like you publish it on a git repository (Github or bitbucket), with a README explaining for example :



  * What you have done

  * How run your project

  * what are the components interact between each over

  * What problems did you have

  * How you would have done things to have the best HA/automated architecture

  * Share with us any ideas you have in mind to improve this kind of infrastructure.


```

Tomorrow we want to put this project in production. What would be your advices and choices to achieve that.

Regarding the infrastructure itself and also external services like the monitoring, ...

```


# My Solution
First i must say , all the required technologies are new to me
And i am trying to learn as fast as possible , which makes me very focised on the requirement alone , and as such i must have fallen into some bad practice

As this prject is ment to show you my work process , and see if align with your company , i wanted to write down th eentire process , including my open questions and dilemas
Looking at the project , i relize it dived into two main parts
1 - the creation of an image by packer and Ansible
2 - managing the image on the cluster with Terraform

First tasks : Need to read about and understand the basics of Terraform , Ansible , Packer , rds database , wordpress , ECS cluster
As i read i writing down my questions (Answers i found , and why):
 1 - Create an Image or a Docker ? (Docker , ECS cluster is basicly AWS version of K8) 
 2 - How to run Ansible from Packer ? (a specific provisioners type for ansible)
 3 - write a basic Ansible playbook and run it from Packer  - and tets you can start that image 
     This should result with Packer ready to go for any Ansible playebook you put into it
	 Found this playbook for wordpress i can use as referance:
	 https://github.com/ansible/ansible-examples/tree/master/wordpress-nginx
 4 - What are the steps required in Ansible to create the wordpress image (
        Found this playbook for wordpress i can use as referance:
         https://github.com/ansible/ansible-examples/tree/master/wordpress-nginx)
 5 - How to set it to work with the rds database?
 6 - what does it means to make it ready to work with the ECS cluster
 7 - test the created image - make sure you have a running wordpress connected to a rds database on 
 8 - Next step - Create the Terraform script to run that image ( It should be redy to push into the ECS cluster)
 9 - to be continued when i fouse on secpond step of project
