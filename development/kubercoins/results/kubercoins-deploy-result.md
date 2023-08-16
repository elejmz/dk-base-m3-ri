# Nombre de la asignación
- Desplegar aplicacion kubercoins

Participantes
- Carlos Lima
- Francisco Pecina
- Miguel Gil
- Diego Ramirez
- Mauricio Barojas
- Iris Jimenez

Actividades
- Instalar la aplicación en un namespace dedicado en el nodo 1.
- Verificar el estado de los nodos del cluster Kubernetes.
- Clonar el repositorio kubercoins.
- Iniciar la aplicación en kubernetes.
- Verificar los logs de los pods aplicativos.
- Navegar al webui.

Comandos
- kubectl get nodes
- cd ~
git clone https://github.com/jpetazzo/container.training
-  kubectl apply -f ~/container.training/k8s/dockercoins.yaml
-  kubectl logs deploy/worker
-  kubectl logs deploy/hasher
-  kubectl get svc webui 
curl 10.111.52.148
-  kubectl get svc webui -o wide
-  kubectl patch svc webui -p '{"spec": {"externalIPs": ["34.220.24.105"]}}'

Recursos externos
- externalIP 34.220.24.105

Artifactos
- Anexar artifactos al directorio de respuesta
