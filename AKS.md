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

Actualizar recurso en kubeconfig
```ssh
	az aks get-credentials --resource-group 'GrupName' --name 'AksName' --subscription 'SuscriptionId' 
	az aks get-credentials --resource-group GRPTestAKS --name Akstest2022 --subscription 996ceb08-b680-4011-888e-c0c1b6abbd02
```

Interacturar con archivo config 
```ssh
	kubectl config view                         # View config file
    kubectl config get-contexts                 # View availables contexts
    kubectl config current-context              # View current context
    kubectl config use-context my-cluster-name  # Switch context
``

Crear namespace
```ssh
	kubectl create namespace <insert-namespace-name-here>
``

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

## Ingress

```ssh
	kubectl get ingress -n namespace           				# View ingress by namespace
	kubectl describe ingress -n namespace <ingress-name>	# View ingress description
```

## Services
```ssh
	kubectl get services -n tracking           				# View services information
```

## Virtual Services
```ssh
	kubectl get virtualservice -n <namespace>      # View virtualservices information
```
