


# Deploying Grafana in okteto cloud

  

## Instructions:

  

1. Install and configure [ okteto CLI ](https://okteto.com/docs/getting-started/installation/) in your host machine.

  

2. Clone the github repo and `cd` to the directory

  

`git clone <> `

  

3. Open the grafana-okteto.yml in your fav text editor and change the namespace field to the name of namespace onto which grafana needs to be deployed.

  
  

Optional: If you're a command line ninja, you can use the below method to change namespace name using sed :

  

`sed '/namespace: /s/:.*$/: your-namespace/' grafana-okteto.yml`

  

4. Deploy the grafana using below command :

  

`kubectl apply -f grafana-okteto.yml`

  

5. Check the newly deployed grafana via `kubectl get pod ` or on okteto cloud web.

  

6. Once the pod is running, in okteto cloud web, a private endpoint will be created for the grafana like https://grafana-namespace.cloud.okteto.net since the service type is loadbalancer.

  

7. Open & login to the grafana in the browser using the private endpoint with credentials `admin/admin`.
