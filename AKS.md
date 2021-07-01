## Initial Configurations

Instalar cli AKS
```ssh
	az aks install-cli
```
Setear el path en DOS y PowerShell
```ssh
	set PATH=%PATH%;C:\Users\user_name\.azure-kubectl"
    $env:path += 'C:\Users\user_name\.azure-kubectl'
```
Login en Azure
```ssh
	az login
```
Obtener credenciales de acceso
```ssh
	az aks get-credentials --resource-group 'GrupName' --name 'AksName' --subscription 'SuscriptionId' 
```
Interacturar con archivo config 
```ssh
	kubectl config view                         # View config file
    kubectl config get-contexts                 # View availables contexts
    kubectl config current-context              # View current context
    kubectl config use-context my-cluster-name  # Switch context
```

## View Resources
Interacturar con archivo config 
```ssh
	kubectl get services                          # List all services in the namespace
    kubectl get pods --all-namespaces             # List all pods in all namespaces
    kubectl get pods -o wide                      # List all pods in the current namespace, with more details
    kubectl get deployment my-dep                 # List a particular deployment
    kubectl get pods                              # List all pods in the namespace
    kubectl get pod my-pod -o yaml                # Get a pod's YAML
```

## Interacting with running Pods

```ssh
	kubectl logs -f my-pod -n namespace           # View container logs
```