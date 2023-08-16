# Nombre de la asignación
-Verificar el estado de los pods

Participantes
- Carlos Lima
- Francisco Pecina
- Miguel Gil
- Diego Ramirez
- Mauricio Barojas
- Iris Jimenez

Actividades
- Crear un namespace para la integración.
- Activar el namespace.
- Obtener los manifests de KuberCoins.
- Añadir el liveness probe al deployment YAML de rng con las siguientes especificaciones:
verbo: Get
path: /
puerto: 80
delay inicial (segundos): 30
periodo (segundos): 5
- Cargar el YAML para todos los recursos de KuberCoins.

Comandos
- kubectl create namespace yellow
- kns yellow
- cd ~
- git clone https://github.com/jpetazzo/kubercoins
- cd kubercoins
- vim rng-deployment.yaml
- Agregar: livenessProbe:
          httpGet:
            path: /
            port: 80
          initialDelaySeconds: 30
          periodSeconds: 5
- kubectl apply -f .
- kubectl get svc rng
- kubectl get events -w
- httping 10.105.58.67
- kubectl get pods -w
- ab -c 10 -n 1000 http://<ClusterIP>/1

Recursos externos
- service/webui    NodePort    10.103.244.85   <none>        80:31976/TCP   27m

Artifactos
- Anexar artifactos al directorio de respuesta
