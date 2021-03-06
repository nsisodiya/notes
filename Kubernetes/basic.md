- A Kubernetes cluster that handles production traffic should have a minimum of three nodes.
- A Kubernetes cluster can be deployed on either physical or virtual machines
- The Deployment instructs Kubernetes how to create and update instances of your application.
- A Deployment is responsible for creating and updating instances of your application
- Once the application instances are created, a Kubernetes Deployment Controller continuously monitors those instances. If the Node hosting an instance goes down or is deleted, the Deployment controller replaces the instance with an instance on another Node in the cluster.
- This provides a self-healing mechanism to address machine failure or maintenance.

# Pod

- Pod can have multiple containers inside. Pod
- All containers in same pod share same ip address. All containers in same pod are tighthly coupled.
- A Pod is a group of one or more application containers (such as Docker or rkt) and includes shared storage (volumes), IP address and information about how to run them.
- Each Pod is tied to the Node where it is scheduled, and remains there until termination (according to restart policy) or deletion. In case of a Node failure, identical Pods are scheduled on other available Nodes in the cluster.

# Node

- Every Kubernetes Node runs at least:
- Kubelet: a process responsible for communication between the Kubernetes Master and the Node; it manages the Pods and the containers running on a machine.
- Container Runtime - Ex Docker

# Commands

- kubectl get - list resources
- kubectl describe - show detailed information about a resource
- kubectl logs - print the logs from a container in a pod
- kubectl exec - execute a command on a container in a pod

- http://localhost:8001/api/v1/namespaces/default/pods/$POD_NAME/proxy/
