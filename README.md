# **Getting Started with MiniShift** 
This is the repository of examples and links that we used for a [Turbonomic Labs](https://turbonomic.com/labs) live stream on July 23, 2020.

MiniShift is a nifty tool for getting started with testing out OpenShift using a local lab so you don't need ot spin up cloud resources or have a dedicated server set up for it.

Here's the YouTube video of the upcoming live session:

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/2ho_Uyh7lnY/0.jpg)](https://www.youtube.com/embed/2ho_Uyh7lnY)


Here's the [app repo we fork in order to use as our sample OpenShift app](https://github.com/turbonomiclabs/ruby-ex)

Here's where you can [download an OC command line for Mac](https://github.com/openshift/origin/releases/download/v3.11.0/openshift-origin-client-tools-v3.11.0-0cbc58b-mac.zip)

Here's where you go to [download the Minishift binary](https://github.com/minishift/minishift/releases)

Here is where you get [VirtualBox](https://virtualbox.org)

If you get an error about your version of VirtualBox, you have to launch the MiniShift using a specific command line here:

```
minishift start --vm-driver virtualbox
```

Here is the commands tha twe use as part of the flow:

Logging in to the CLI as admin:
```
oc login -u system:admin
```

Deploying our ruby-ex sample app (replace the URL with your forked repo url)
```
oc new-app openshift/ruby:2.5~https://github.com/turbonomiclabs/ruby-ex
```