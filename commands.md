# Kubernetes Commands

## kubectl

```bash
 kubectl get nodes
```
- This is to see how many nodes are running in the cluster

```bash
kubectl run nginx --image=nginx
```
- This pull down a container image from public(Docker Hub) or private repository and creates a pod

```bash
kubectl get pods
```
- This will get information about the pods running on the cluster.


# Declarative Approach

##### This means creating a script to create and deploy application which allows for version control.

Kubernetes uses .yaml files:

- For Example

***pod-definition.yml***
```yaml
apiVersion:
kind:
metadata:
    name: myapp-pod
    labels:
        app: myapp
        type: front-end

spec:
    containers:
        - name: nginx-container
          image: nginx

```
```bash
kubectl create -f pod-definition.yml
```
- This creates the pod based on the yaml file specified

