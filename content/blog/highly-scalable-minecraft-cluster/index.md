+++
title = "Highly scalable Minecraft cluster"
date = 2023-11-03
updated = 2023-11-03
description = "How to build and configure a highly scalable Minecraft server"

[taxonomies]
tags = ["kubernetes", "minecraft", "cluster"]

[extra]
pinned = true
toc = false
quick_navigation_buttons = true
+++
Are you planning a very large Minecraft LAN party? Then this article is for you. Here I show you how to set up a highly scalable Minecraft cluster.


### What is a Minecraft cluster?

A Minecraft cluster is a Minecraft server network that consists of multiple Minecraft servers. These servers are connected to each other via a network and can therefore be shared. This means that you can play with your friends on a server that consists of multiple servers.

### How does a Minecraft cluster work?

A Minecraft cluster consists of several components. 

<!-- Image -->
![Minecraft cluster](https://github.com/MultiPaper/MultiPaper/raw/main/assets/multipaper-diagram.jpg)

#### Master database
First, there is the master database. This database allows servers to store data in a central location that all servers can access. Servers store chunks, maps, level.dat, player data, banned players, and more in this database. This database also records which chunk belongs to which server and coordinates communication between servers.

#### Server
The master database is great for storing data, but not so good at synchronizing data in real time between servers. This is where peer-to-peer communication comes in. Each server establishes a connection to another server so that data between them can be updated in real time. When a player on server A attacks another player on server B, server A sends this data directly to server B so that server B can damage the player and apply any knockback.

#### Load Balancer
The load balancer is the last component of the cluster. A load balancer is required to distribute players evenly across your servers. A load balancer automatically distributes players between servers to distribute the load evenly across the individual servers.

### Why do I need multiple servers?
By having multiple servers, we can distribute the load across multiple servers. This means that we can have more players on our servers without the servers becoming overloaded. With this setup, we can also easily add new servers if we get more players. If the number of players decreases again, the server can be removed again.

## Preparation

You should be familiar with Kubernetes and have set up a Kubernetes cluster. I recommend [k3s](https://k3s.io/).

You should also be familiar with Helm. I recommend [Helm 3](https://helm.sh/docs/intro/install/).

## Installation

First, you should clone the repository.

```bash
git clone git@github.com:alexohneander/MultiPaperHelm.git
cd MultiPaperHelm/
```

I installed the entire setup in a separate namespace. You can create this namespace with the following command.

```bash
kubectl create namespace minecraft
```

Next, we install the Minecraft cluster with Helm.

```bash
helm install multipaper . --namespace minecraf
```

Once the Helm chart is installed, you can view the port of the proxy service.

```bash
kubectl describe service multipaper-master-proxy -n minecraft
```

This port is the port that you need to enter in your Minecraft client.

## Configuration

The Helm chart creates several ConfigMaps. In these ConfigMaps, you can customize the configuration of your cluster.

For example, you can set the number of maximum players or change the description of the server.

For more information on the individual config files, see [MultiPaper](https://github.com/MultiPaper/MultiPaper).

## Conclusion

With this setup, you can easily set up a highly scalable Minecraft cluster. You can easily add new servers if you get more players and remove them again if the number of players decreases again.

You can test this setup under the following Server Address: `minecraft.alexohneander.de:31732`

If you have any questions, feel free to contact me on [Email](mailto:moin@wellnitz-alex.de) or on [Matrix](https://matrix.to/#/@alexohneander:dev-null.rocks).