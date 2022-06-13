## Initial Configurations
Instalar cli AKS
```ssh
	az aks install-cli
```
Setear path at DOS & PowerShell
```ssh
	set PATH=%PATH%;C:\Users\user_name\.azure-kubectl"
   	$env:path += 'C:\Users\user_name\.azure-kubectl'
```
Login on Azure
```ssh
	az login
```
Get access credentials
```ssh
	az aks get-credentials --resource-group 'GrupName' --name 'AksName' --subscription <SuscriptionId> 
```

## Update resource on kubeconfig file
```ssh
	az aks get-credentials --resource-group 'GrupName' --name 'AksName' --subscription 'SuscriptionId' 
```

## Interacting with config file
```ssh
	kubectl config view                         # View config file
    	kubectl config get-contexts                 # View availables contexts
    	kubectl config current-context              # View current context
    	kubectl config use-context my-cluster-name  # Switch context
```

## Create a new namespace
```ssh
	kubectl create namespace <insert-namespace-name-here>
```

## View Resources
```ssh
	kubectl get services                          # List all services in the namespace
   	kubectl get pods --all-namespaces             # List all pods in all namespaces
    	kubectl get pods -o wide                      # List all pods in the current namespace, with more details
    	kubectl get deployment my-dep                 # List a particular deployment
    	kubectl get pods                              # List all pods in the namespace
    	kubectl get pod my-pod -o yaml                # Get a pod's YAML
	kubectl get gateway -n <namespace>            # List all gateway in namespace
	kubectl get virtualservice -n <namespace>     # List all virtualservices information
```

## Interacting with running Pods
```ssh
	kubectl logs -f my-pod -n namespace           # View container logs
```

## Ingress
```ssh
	kubectl get ingress -n namespace           				# View ingress by namespace
	kubectl describe ingress -n namespace <ingress-name>	# View ingress description
```
