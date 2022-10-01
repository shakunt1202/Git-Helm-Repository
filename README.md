
![](https://community-cdn-digitalocean-com.global.ssl.fastly.net/GVfcoCn7JqkP5UD8hUZ3Lcg7)

<h2>Introduction</h2> 

Deploying applications to Kubernetes – the powerful and popular container-orchestration system – can be complex. Setting up a single application can involve creating multiple interdependent Kubernetes resources – such as pods, services, deployments, and replicasets – each requiring you to write a detailed YAML manifest file.

Helm is a package manager for Kubernetes that allows developers and operators to more easily package, configure, and deploy applications and services onto Kubernetes clusters.

Helm is now an official Kubernetes project and is part of the Cloud Native Computing Foundation, a non-profit that supports open source projects in and around the Kubernetes ecosystem.

In this article we will give an overview of Helm and the various abstractions it uses to simplify deploying applications to Kubernetes. If you are new to Kubernetes, it may be helpful to read An Introduction to Kubernetes first to familiarize yourself with the basics concepts.

An Overview of Helm
Most every programming language and operating system has its own package manager to help with the installation and maintenance of software. Helm provides the same basic feature set as many of the package managers you may already be familiar with, such as Debian’s apt, or Python’s pip.

<h3>Helm can:</h3>

<li>Install software.
<li>Automatically install software dependencies.
<li>Upgrade software.
<li>Configure software deployments.
<li>Fetch software packages from repositories.
<li>Helm provides this functionality through the following components: 

    A command line tool, helm, which provides the user interface to all Helm functionality.
    A companion server component, tiller, that runs on your Kubernetes cluster, listens for commands from helm, and handles the configuration and deployment of software releases on the cluster.
    The Helm packaging format, called charts.
    An official curated charts repository with prepackaged charts for popular open-source software projects.
    We’ll investigate the charts format in more detail next.

<h3>Charts</h3>
Helm packages are called charts, and they consist of a few YAML configuration files and some templates that are rendered into Kubernetes manifest files. Here is the basic directory structure of a chart:

