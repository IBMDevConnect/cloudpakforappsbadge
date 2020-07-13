## Introduction

In this lab, you will learn about how to define Continuous Integration for your application. We are using [Jenkins](https://jenkins.io/) to define it.

### Jenkins

Jenkins is a popular open source Continuous Integration tool. It is built in Java. It allows the developers to perform continuous integration and build automation. It allows you to define steps and executes them based on the instructions like building the application using build tools like Ant, Gradle, Maven etc, executing shell scripts, running tests etc. All the steps can be executed based on the timing or event. It depends on the setup. It helps to monitor all these steps and sends notifications to the team members in case of failures. Also, it is very flexible and has a large plugin list which one easily add based on their requirements.

Check these guides out if you want to know more about Jenkins - [Jenkins, Leading open source automation server](https://jenkins.io/doc/).

## Prerequisites

- You need an [IBM cloud account](https://cloud.ibm.com/login).
- You should be familiar with basics like Containers, Docker, Kubernetes.

## Continuous Integration

To proceed with today's workshop

1) Login to below mentioned link-

<https://www.katacoda.com/jbmatthews/courses/jenkins/>

2) Navigate to "Build Docker Images with Jenkins" and Click on Start Scenario.

Sign up with any one of the options for Katakoda platform.
Here you'll learn how to configure Jenkins to build Docker Images based on a Dockerfile. The scenario is designed to demonstrate how you can use Docker within a CI/CD pipeline, using Images as a build artifact that can be promoted to different environments and finally production.

### Various stages covered in this scenarios are-

1) Launch Jenkins

2) Configure Docker Plugin

3) Add Docker Agent

4) Create Build Project

5) Build Project

6) View Console Output

Start performing the lab .
