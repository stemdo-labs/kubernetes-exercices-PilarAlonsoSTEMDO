 C:\Users\palonso\Desktop\Workspace_VSC\KUBERNETESSEMANALES\kubernetes-exercices-PilarAlonsoSTEMDO\soluciones\ejercicio3> kubectl apply -f pod-apache.yml
pod/apache-yaml created
PS C:\Users\palonso\Desktop\Workspace_VSC\KUBERNETESSEMANALES\kubernetes-exercices-PilarAlonsoSTEMDO\soluciones\ejercicio3> kubectl get pods -o wide
NAME          READY   STATUS    RESTARTS   AGE   IP           NODE       NOMINATED NODE   READINESS GATES
apache-yaml   1/1     Running   0          30s   10.244.0.5   minikube   <none>           <none>
PS C:\Users\palonso\Desktop\Workspace_VSC\KUBERNETESSEMANALES\kubernetes-exercices-PilarAlonsoSTEMDO\soluciones\ejercicio3> kubectl port-forward pod/apache-yaml 8080:80
Forwarding from 127.0.0.1:8080 -> 80
PS C:\Users\palonso\Desktop\Workspace_VSC\KUBERNETESSEMANALES\kubernetes-exercices-PilarAlonsoSTEMDO\soluciones\ejercicio3> kubectl delete pod apache-yaml
pod "apache-yaml" deleted