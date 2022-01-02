# containers
[[LXC-LXD]]
[[CoreOS]]

## basics
- portable software
- consistent and reliable environment to run software
- similar to virtual machines, less overhead.
- run directly on host machine (usually Linux.)

## container orchestration
- tool. eg, kubernetes.
- in old days: Server down -> Perform Deployment -> Server up
- zero-downtime deplotment: 
	- -> spin up containers running new code
	- -> direct user traffic to the new containers
	- -> remove old containers running old code.

### tools
- [[docker]]
- [[kubernetes]]
	- alternatives:
		- docker swarm
		- Marathon
			- https://mesosphere.github.io/marathon/
		- Nomad (by HashiCorp)
			- https://nomadproject.io

## why?
- software portability
	- run s/w consistently on different machines.
- isolation
	- keeping individual pieces of s/w seperate from one another.
- scaling
	- increase/decrease resources alocation as needed. 
- automation
	- automating processes to save money.
- efficient resource usage
	- containers use resources efficiently -> saves money
## pros / advantages
- isolation and portability of vms
- lightweight than vms
- faster than vms - can start up in seconds
- smaller than vms
- faster and simpler automation
## cons / advantage
- less flexibility than vms.
- new challenges around orchestration and automation
	- tools like kubernetes support this out of the box
## container runtime
- [[docker]]
- rkt (pronounced rocket)
	- created by CoreOS (acquired by RedHat)
	- https://coreos.com/rkt -> RH OpenShift
- containerd
	- does not have container-image management.
	- https://containerd.io
- podman

## use cases
### microservices
- split the application into a series of small, independant services.
- can be built, modified and scaled seperately.
- orchestration excel when it comes to managing a large number of small, independent workloads.
- containers and orchestration make it easier to manage and automate the process of deploying, scalingm and connecting lots of microservice instances.
### cloud transformation
- process of migrating your existing IT infrastructure to the cloud.
- containers can wrap existing software in containers.
### automated scaling
- refers to automatically provisioning resources in response to real-time data metrics.
- reduce cost from business perspective
### continous deployment pipeline
- practice of deploying new code automatically and frequently. 
- containers work very well in the context of continous deployment.
- automation pipeline.
### self-healing apps
- automatically identify problems and take steps to correct it
- replace broken containers with new ones instantly.
### developer visibility
- containers are identical to production environment.
- devs have the ability to test their code and see how it will behave in production.

## cloud
- just means someone else's computer.
- cloud providers -> AWS, Azure, GCP. Also, DigitalOcean, Vultr, Linode.
	- AWS
		- ECS
		- EKS (kubernetes)
	- Azure
		- AKS (kubernetes)
	- GCP
		- GKE (kubernetes)
- with cloud providers, you only pay for what you use. 
	- use less resources, pay less
- cloud platforms provides support out-of-the-box.