# Scalable GitLab Runners

- By: Filip Procházka
- When: Saturday, 12:00

## Runner types

- shell
- ssh
- virtual box
- parallels
- docker (**FTW!**)
- kubernetes
- custom (eh)

## Docker machine (fine, but deprecated)

- deprecated
- gitlab fork, kinda ok, wanted to be dropped

## AWS

- vpc
- ec2 spot instances
- cheap af
- many instance types

### EC2 Spot

- single AZ
- some waiting cuz of docker-machine

### EC2 Spot Fleet

- multiple AZ
- more flexible then spot
- docker-machine does not support ec2 spot fleet

## IRL setup

### Master runner

- leader
- micro instance
- "job scheduler"
- gitlab-runner && docker-machine

### Worker

- ec2 spot (fleet) instance with docker
- managed by docker-machine
- custom [Filip Prochazka](https://filip-prochazka.com)'s docker-machine plugin, to allow ec2 spot fleet management
