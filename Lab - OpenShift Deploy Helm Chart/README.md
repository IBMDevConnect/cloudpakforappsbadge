## Prerequisites

- You will need an IBM Account for [IBM Cloud](https://cloud.ibm.com/)
- Downloaded and installed the IBM Cloud CLI at [IBM Cloud CLI Installation](https://cloud.ibm.com/docs/cli?topic=cloud-cli-getting-started#step1-install-idt). Follow the instructions for your computer’s operating system.
- Downloaded and installed the Helm CLI at [Helm CLI Installation](https://github.com/helm/helm#install).
- Downloaded and installed the Kubernetes CLI at [Kubernetes CLI Installation](https://kubernetes.io/docs/tasks/tools/install-kubectl/). Follow the instructions for your computer’s operating system.

## Getting the Sample Application

Download the sample application from Github: [Sample App](https://github.com/ibm-cloud-architecture/cloudnative_sample_app)

## Deploying the Sample Application using Helm

In this section we will deploy the sample application that you downloaded using the Helm CLI in your terminal or cmd prompt. The helm charts are already pre-created in the `/chart` directory of the application directory.

### Checking the Namespace

To check the namespace you are deploying your application to run the following command:

View Namespace

```shell
oc projects
```

Create A Project

Once logged in, we want to create a new project called deploy-sample in your OpenShift Cluster:

```shell
oc new-project deploy-sample
```

If you already have an existing project, you can select the project using:

```shell
oc project deploy-sample
```

Get the Sample Application from Github

Always double check the namespace your Kubernetes is set for to make sure you are deploying the application where you would like it to be in your Kubernetes Cluster.

### Clone the sample project

```shell
git clone https://github.com/ibm-cloud-architecture/cloudnative_sample_app
```

### Application Deployment

To deploy the Application we first want to ensure that we have helm template charts created. In this sample app we won’t have to create any templates, but we are going to modify the deployment.yaml using templates. Let’s start by doing that.

In the `chart/cloudnativesampleapp` directory in your sample application run:

#### Changing Replica Count

```shell
helm template . --set replicaCount=2 > deployment.yaml
```

That will set the replicaCount in the deployment file to 2. Next we need to deploy the new change by running the following:

#### Deploy Deployment

```shell
oc apply -f deployment.yaml
```

And that’s it. You have now deployed using a Helm Template.

To verify your deployment just run:

#### Verify Deployment

```shell
oc get deployment
```

### Accessing the Application

To access the application we need to expose the service. To do that we will run the following:

#### Expose Service

```shell
oc expose service cloudnativesampleapp-service
```

Next, we need to find the route that was exposed for the application. We find that by running:

#### Service Route

```shell
oc get route
```

Next copy the `PATH` it will look similar to `greeting-service-deploy-sample.gse-cloud-native-fa9ee67c9ab6a7791435450358e564cc-0001.us-east.containers.appdomain.cloud`. Finally we want to run a `curl` against the copied path with `/greeting` appended on the end to see the response.

#### Curl

```shell
curl PATH/greeting
```

You should get a response similar to: `Welcome to Cloudnative bootcamp !!!`

## Conclusion

You have successfully completed this lab! Let’s take a look at what you learned and did today:

- Modified a Helm Chart value.
- Deployed an application using a Helm Chart.
- Exposed the application to the internet.
- Accessed the deployed application via a CURL command.
