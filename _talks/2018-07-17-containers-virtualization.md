---
title: "Containers & Virtualization"
collection: talks
type: "Tutorial"
permalink: /talks/2018-07-09-containers-virtualization
venue: "Media.net"
date: 2018-07-17
location: "Mumbai, India"
---

The tutorial was conducted for the training session for the new DevOps hires at media.net. Please find the slides here

[Containers](files/Containers.pdf)

[Virtualization](files/Virtualization.pdf)

Test
====

1. Create a memory hungry application (systemd-service), try to limit it's resources using cgroups and create a separate proc namespace to isolate processes. [10 points]

    ### Learning objectives:
    By the end of the exercise, you should learn about
    1. Cgroups - resource limitation
    2. Namespaces - isolation of subsystems
    3. Process trees, systemd
    
    Do the same using docker containers. [10 points]
    
2. Nextcloud is an OpenSource private self-hosted storage solution akin to Dropbox. A Nextcloud deployment typically contains a web proxy, mysql, a php application, and the letsencrypt certbot for automated TLS certificate renewals. Deploy a Nextcloud instance using containers (You may use a Dockerfile or docker-compose, up to you). You may skip deploying the TLS certificate generator / renewal bot  (letsencrypt-nginx-proxy-companion) if you don't want to support TLS / HTTPS (EFF's certbot).

    `Hint 1`: Nextcloud is OpenSource.

    `Hint 2`: HTTPS is usually configured to run on port 443.
    
    `Hint 3`: Hint for hint 1: https://github.com/nextcloud/docker/tree/master/.examples

    `Submit` your Dockerfiles / docker-compose files and nextcloud deployment endpoints.

    ### Learning objectives:

    By the end of the exercise, you should learn about
    1. Containerizing deployment and application parts - resource limiting, isolation, efficient usage
    2. stateless vs stateful architecture - volume mounts
    2. basics of overlay networks

    [40 points]

    Bonus: Try to make the deployment stateless. [40 points]

3.  Create two namespaces providing veth (Virtual Ethernet drivers) isolation, so that the two containers are able to ping each other.

    ### Learning objectives:

    By the end of the exercise, you should learn about
    1. Container networking
    
    `Submit` screenshots of ping trace / dockerfiles / configuration used.
    
    [30 points]
    
4. Bake a Cloudstack Image to spin up a VMs(KVM) with attached volumes, each with a random hostname which shouts the box's hostname on flock after it comes up.

    ### Learning objectives:
    By the end of the exercise, you should learn about
    1. How CloudStack spins up VMs? Storage provisioning?
    2. User data scripts
    3. system runlevels
    4. flock bots (lol)
    
    `Submit` your Imageid and your flockbot name.
     
    [40 points]
