# creo el yml y después ejecuto:
PS C:\Users\palonso\Desktop\Workspace_VSC\KUBERNETESSEMANALES\kubernetes-exercices-PilarAlonsoSTEMDO\soluciones\ejercicio2> kubectl apply -f pod-apache.yml
pod/apache created
# LISTAR PODS
PS C:\Users\palonso\Desktop\Workspace_VSC\KUBERNETESSEMANALES\kubernetes-exercices-PilarAlonsoSTEMDO\soluciones\ejercicio2> kubectl get pods
NAME     READY   STATUS    RESTARTS   AGE
apache   1/1     Running   0          52s
# DESCRIPCIÓN DEL POD
PS C:\Users\palonso\Desktop\Workspace_VSC\KUBERNETESSEMANALES\kubernetes-exercices-PilarAlonsoSTEMDO\soluciones\ejercicio2> kubectl describe pod apache
Name:             apache
Namespace:        default
Priority:         0
Service Account:  default
Node:             minikube/192.168.49.2
Start Time:       Mon, 13 May 2024 13:39:12 +0200
Labels:           <none>
Annotations:      <none>
Status:           Running
IP:               10.244.0.4
IPs:
  IP:  10.244.0.4
Containers:
  apache:
    Container ID:   docker://206c5174334bc8f39cdbad0f5929b1d77575c587626a0846d889e4993321e155
    Image:          httpd
    Image ID:       docker-pullable://httpd@sha256:36c8c79f900108f0f09fd4148ad35ade57cba0dc19d13f3d15be24ce94e6a639
    Port:           <none>
    Host Port:      <none>
    State:          Running
      Started:      Mon, 13 May 2024 13:39:16 +0200
    Ready:          True
    Restart Count:  0
    Environment:    <none>
    Mounts:
      /var/run/secrets/kubernetes.io/serviceaccount from kube-api-access-xwsln (ro)
Conditions:
  Type              Status
  Initialized       True
  Ready             True
  ContainersReady   True
  PodScheduled      True
Volumes:
  kube-api-access-xwsln:
    Type:                    Projected (a volume that contains injected data from multiple sources)
    TokenExpirationSeconds:  3607
    ConfigMapName:           kube-root-ca.crt
    ConfigMapOptional:       <nil>
    DownwardAPI:             true
QoS Class:                   BestEffort
Node-Selectors:              <none>
Tolerations:                 node.kubernetes.io/not-ready:NoExecute op=Exists for 300s
                             node.kubernetes.io/unreachable:NoExecute op=Exists for 300s
Events:
  Type    Reason     Age   From               Message
  ----    ------     ----  ----               -------
  Normal  Scheduled  71s   default-scheduler  Successfully assigned default/apache to minikube
  Normal  Pulling    70s   kubelet            Pulling image "httpd"
  Normal  Pulled     67s   kubelet            Successfully pulled image "httpd" in 3.31s (3.31s including waiting)
  Normal  Created    67s   kubelet            Created container apache
  Normal  Started    67s   kubelet            Started container apache
  # BORRAR POD
PS C:\Users\palonso\Desktop\Workspace_VSC\KUBERNETESSEMANALES\kubernetes-exercices-PilarAlonsoSTEMDO\soluciones\ejercicio2>
 kubectl delete pod apache

pod "apache" deleted