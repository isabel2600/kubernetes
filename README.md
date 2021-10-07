# kubernetes

#K3s kubernetes installation


# how to run:
$curl -sfL https://get.k3s.io | sh -

$k3s kubectl get node

$sudo k3s kubectl get node

#  Place to test Kubernet
$sudo su

$kubectl --kubeconfig /etc/rancher/k3s/k3s.yaml get pods --all-namespaces

$sudo kubectl --kubeconfig /etc/rancher/k3s/k3s.yaml get pods --all-namespaces

# Create a deployment

$sudo kubectl create deployment test-dockerdemo --image=sirfragalot/docker-demo:dcus

$sudo kubectl get pods

$sudo kubectl exec test-dockerdemo-588b8d99d-zvnjt  -- env 

$sudo kubectl exec test-dockerdemo-588b8d99d-zvnjt  -- /sbin/env 

# Scale the replicas
$sudo kubectl scale deployment  test-dockerdemo --replicas=5
 
# Viewing Pods
 sudo kubectl get pods

# Expose the application port
$kubectl expose deployment test-dockerdemo --type="NodePort" --port 8080

$kubectl get services test-dockerdemo

-command output
test-dockerdemo   NodePort   10.43.232.211   <none>        8080:32266/TCP   2d18h

# Put this ip address in your brownser and you will see the 5 containers running
 
![image](https://user-images.githubusercontent.com/68034656/136408169-8678d581-b151-4240-863f-5b030aac14e5.png)

