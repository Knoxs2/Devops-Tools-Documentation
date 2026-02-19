# Overall knowledge

## Core dimensions

### Systems Thinking - How everything connects

#### SDLC - Planning & Requirement
    Define a deployment strategy (Where the app will run, Multi-region, HA Strategy, Cost Model)
    Choose a infrastructure Model ()
    Define a environment Strategy (Dev, QA, Staging, Production) [Number of environments, Isolation Level, Naming conventions, Promotion Strategy]
    Define Branching & Release strategy (Git flow vs trunk based, PR requirements, Tagging model, Release cadence)
    Define Devops Toolchain
    CI/CD Architecture
    Infrastructure as Code Strategy
    Secrets Management
    Monitoring & Logging Strategy
    High-level cloud architecture

#### SDLC - Design Phase
    Collaboration on System architecture
    Review Scalability and availability design
    define containerization strategy
    define networking and security model
    Cloud architecture (VPC,subnets, load balancers)
    Auto-scaling Strategy
    Backup & disaster recovery strategy
    Zero-downtime deployment model

#### Development Phase
    Provide automated build systems
    Enforce code quality & Security Checks
    Standardize development environments
    Implement container build processes
    CI Pipelines (build + test automation)
    Code Scanning (SAST/DAST)
    Docker Builds standards
    Artifact repository strategy
    Shift left Security
    Reproducible builds
    Developer Productivity

#### Testing Phase
    Automate test execution
    provide ephemeral environments
    Performance & load testing automation
    Automated environment provisioning
    test data management
    load testing pipelines
    integration testing pipelines

#### Deployment Phase
    Automate deployments
    Implement safe release strategies
    ensure rollback capability
    CI/CD Pipelines
    Blue-green deployment
    Canary Releases
    feature flags integration
    Zero manual deployments
    one click rollback
    versioned infrastructure
#### Operations & Monitoring Phase
    System monitoring
    Logging & alerting
    Incident response
    Performance optimization
    Centralized Logging
    Metrics & Dashboard
    Alert Strategy
    SLO/SLA definitions
    Latency
    Traffic
    Errors
    Saturation
    
### Production Awareness

* failure
* Scaling
* logs
* monitoring

## Linux

### Important Commands

top --- List processes and system resources usage
htop --- Modern imagination of top, colors
ps aux --- Processes in execution with + other users that have CPU/RAM usage
awk --- text processing, data extraction, reporting
lsof --- list open files -> arquivos abertos, diretorios, sockets de rede, pipes, redes ativas
ss --- socket statistics -> investigate network sockets TCP, UDP and UNIX SOCKETS
kill --- Kills processes
grep --- global regular expression unit -> Search for specific text patterns in files or data streams
sed --- Stream editor for parsing text and transforming text

### Concepts

load average -> metric that measure number of tasks that are running or waiting for system resources
CPU Usage -> metric for CPU usages
Boot process ->
SIGNALS -> "signal" sent to a process to notify of an event
Hard Link -> direct reference to a file data on disk
Soft Link -> Special file that serves as a pointer to another file



## Networking Concepts

### Core Concepts

* LB L4 (Route traffic based on network data(IP, PORT, TCP/UDP FOR HIGHSPEED PERFORMANCE)
* LB L7 (Analyze application Layer-data, URLS, cookies, HTTP headers to make inteliggent decisions)
* NAT (Network Address Translation, enable multiple devices on a private network to use a unique public IP for internet access)


## COntainers


### Core Concetps

* Diferrence between VM and Container (VM Virtualizes entire machine, Containers virtualize only software layers)
* CMD vs Entrypoint ( Entrypoint always runs, CMD can be overriden on runtime)
* Multistage Build ( Use multi stage FROM statements)
* container communicate (Virtual networks, virtual bridges, internal DNS service discovery)


## Kubernetes

### Core Concepts
* Kube-proxy -> Direct traffic to proper pod
* etcd -> controls the state of the cluster, data store and single source of truth
* Liveness probe -> check if is alive
* readiness probe -> check if is active
* Rolling update -> update applications with zero downtime by incrementally replacing old pods

### Ingress
* Load Balancer vs Ingress
* Ingress (API Object, manages external access to services within a kubernetes cluster) Define Ingress resource to define rules of the load balancing and Ingress controller (software component NGINX, Traefik or HAProxy) watches for the ingress resources and apply the rules defined
* Ingress Cost Efficient

### Service Mesh

* Sidecar proxies injected into pods, that manages microservice communication to provide enhanced security, observability and traffic management without changing application code

### HELM
* Package manager to simplify deployment, managements, versioning of appplications
* Charts is a Helm package, Yaml manifest containing information necessary
* Release -> instance of a chart running in kubernetes
* Templatization of kubernetes manifest, to quickly deploy applications based on values.yaml
* External Secrets Operator -> Install on cluster and it automatically fetch from external secrets manager
* Can have private repository, using external tool, Artifact repository or even Github repository

## CI/CD

### Core Concepts

* Pipeline -> automated workflow that integrate code changes, running tests, deploy applications
* How to secure secrets -> Use secret managers or Native Secret managers in CI/CD Tools
* Blue/green -> zero-downtime deployment strategy that swaps 100% of the traffic between two identical environments
* Canary -> gradually rolls out changes for a small portion of the users
* when to use each -> blue/green new versions, Canaray test new features with real users

### Gitops

* uses git as single source of truth for Infrastructure and applications
* Install via yaml manifest directly into kubernetes
* Sync by getting state difference in a repository and live kubernetes cluster


## GIT

### Core Concepts
* Rebase -> moves feature branch commits to the tip of the main
* Merge -> merge commit with all the features


## Observability & Monitoring

* Monitoring (Track metrics, logs and traces)
* Logging (Get logging information of the applications, and can centralize using Kibana for example)
* Tracing (Follows the path of a request as it flows for multiple services, delays, bottlenecks, failures)
* Observability (Ability to infer internal state of a complex system, examing its external outputs telemetry data)
* Telemetry data (Metrics, events, Logs, traces)

