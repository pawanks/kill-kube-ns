# Env info 

~~~sh
Client Version: version.Info{Major:"1", Minor:"8", GitVersion:"v1.8.7", GitCommit:"b30876a5539f09684ff9fde266fda10b37738c9c", GitTreeState:"clean", BuildDate:"2018-01-16T21:59:57Z", GoVersion:"go1.8.3", Compiler:"gc", Platform:"darwin/amd64"}
Server Version: version.Info{Major:"1", Minor:"13", GitVersion:"v1.13.4", GitCommit:"c27b913fddd1a6c480c229191a087698aa92f0b1", GitTreeState:"clean", BuildDate:"2019-02-28T13:30:26Z", GoVersion:"go1.11.5", Compiler:"gc", Platform:"linux/amd64"}
~~~
# kill-kube-ns

Kill a Kubernetes namespace/OpenShift project which is stuck in the state of "Terminating".

Also see: [kubernetes/kubernetes#60807](https://github.com/kubernetes/kubernetes/issues/60807)

This scripts automates the steps suggestes by some people on the comments of the issue.

**Note:** Use at your own risk! It works for me though.

## Usage

~~~sh
./kill-kube-ns myproject
~~~

**Note:** You will need to be logged in to your cluster, and have the necessary permissions. Make sure that your port `8001` is available.

## Pre-requisites

Your will need to have the following things installed:

* bash
* curl
* jq
* kubectl
