# tickets-of-k8s
	1. Kubectl create -f kuard-rs-test.yaml
	2. Kubectl get rs -o wide
	3. Kubectl get pods --show-labels
	4. Kubectl get services -o wide
	5. Kubectl get endpoints
	So the system idea is you should more pay attention for labels only
	Emphemeral=keep changing ip of pods or died
	Services = are our load balancers
	NodePort - is a service type
	Load balancer has his own external IP
	Behind load balance run nodes port
Ingress send to service and service to pods
______________________________________________________________________________________________________________
   echo -n 'secret-creds' > ./username.txt
   echo -n 'MySecureP@ss' > ./password.txt
   kubectl create secret generic secret-creds --from-file=./username.txt --from-file=./password.txt
   kubectl delete secrets secret-creds
   kubectl create secret generic secret-creds --from-file=./username.txt --from-file=./password.txt
   kubectl get secrets
   cat ./username.txt
   kubectl get pods
   vi secrets-redis.yaml
   kubectl delete secrets-redis.yaml
   kubectl delete pod redis-pod
   kubectl create -f secrets-redis.yaml
   kubectl get pods
   kubectl get secrets
   kubectl describe secrets secret-creds
   kubectl get pods
   kubectl delete pod secrets-redis.yaml
   kubectl get pods
   kubectl exec -it redis-pod /bin/bash
