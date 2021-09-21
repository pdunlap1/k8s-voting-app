# k8s-voting-app overview
My k8s project for implementing the example voting app in GKE and Kubernetes. This is a simple distributed application running across multiple Docker containers orchestrated and administered with GKE.

# Purpose 
The purpose of this project is to deploy a voting app and results app using kubernetes and GCP/GKE. Participants will access the voting platform through a front-end web app 

See original example-voting-app link here for in-depth details on app architecture : https://github.com/dockersamples/example-voting-app

# App architecture
- A front-end web app in Python or ASP.NET Core which lets you vote between two options
- A Redis or NATS queue which collects new votes
- A .NET Core, Java or .NET Core 2.1 worker which consumes votes and stores them in…
- A Postgres or TiDB database backed by a Docker volume
- A Node.js or ASP.NET Core SignalR webapp which shows the results of the voting in real time


# Why I created this project
After creating multiple projects, clusters, and different configs inside GCP, I could not get the example-voting-app k8s-specifications to run the deployments and services correctly. I could see both of the voting-app and the results-app, but every time I input a vote, no changes would show in the results app. Somewhere in the chain, the redis, worker, or postgres pods were non-funcitoning. I believe this was due to deprecated APIs that were no longer working with GCP. So to get around this, I scripted the apps in RubyMine with the correct APIs, uploaded those deployments and pods to this Github repo, and 

