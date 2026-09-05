# CodeAlpha_JenkinsRemoting
Jenkins Remoting project demonstrating CI/CD automation using Jenkins and Docker agents for remote build execution.

# Jenkins Remoting with Docker Agent

A hands-on DevOps project demonstrating Continuous Integration (CI) using Jenkins, Docker, AWS EC2, and GitHub.

---

## AWS EC2 Setup

First, I created an AWS EC2 instance using the Ubuntu operating system. This EC2 instance was used to host the Jenkins server.

The required instance configuration and security group settings were configured to allow access to the server.

![Creating AWS EC2 Instance](screenshots/Creating_Instance_1.png)

## Connecting to EC2

After creating the EC2 instance, I connected to the Ubuntu server using SSH through the terminal.

This allowed me to access the EC2 instance and perform the required Jenkins and Docker setup.

![Connecting to EC2](screenshots/Connecting_to_EC2_2.png)

## Java Prerequisite

Before installing Jenkins, Java 17 was installed on the Ubuntu EC2 instance because Jenkins requires Java to run.

The Java installation was verified using the `java -version` command.

```bash
sudo apt update
sudo apt install openjdk-17-jre -y
java -version


### Upload the third screenshot

Inside your existing `screenshots` folder, upload:

```text
pre-requisite_for_jenkins_3.png
