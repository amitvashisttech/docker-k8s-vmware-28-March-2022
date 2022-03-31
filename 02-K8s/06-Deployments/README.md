 ``` 
  123  cd 06-Deployments/
  124  ls
  125  vim helloworld.yaml
  126  kubectl  get pods 
  127  kubectl  get ns 
  128  kubectl  get pods -n kube-system
  129  kubectl  get pods -n kube-system --kubeconfig=/etc/kubernetes/admin.conf 
  130  ls
  131  kubectl  apply -f helloworld.yaml 
  132  kubectl  get deployment 
  133  kubectl  get pods 
  134  kubectl desribe pod helloworld-deployment-6df7c6f5bb-v2gnd
  135  kubectl describe pod helloworld-deployment-6df7c6f5bb-v2gnd
  136  ls
  137  kubectl scale --replicas=2 helloworld.yaml 
  138  kubectl scale --replicas=2 -f helloworld.yaml
  139  kubectl  get pods 
  140  kubectl  get pods -o wide 
  141  kubectl  get pods 
  142  ls
  143  cd /root/.kube/
  144  ls
  145  cp -rf config ../eks-cfg
  146  s
  147  l
  148  cd 
  149  ls
  150  cp -rf /etc/kubernetes/admin.conf .kube/config
  151  kubectl get pods 
  152  kubectl delete rc --all
  153  ls
  154  cd docker-eks-verizon-14-March-22/
  155  ls
  156  cd 02-K8s/
  157  ls
  158  cd 06-Deployments/
  159  s
  160  kubectl apply -f 06
  161  kubectl apply -f helloworld.yaml 
  162  kubectl get pods 
  163  kubectl get deploy,rs,pod 
  164  kubectl  describe deploy helloworld-deployment
  165  kubectl get deploy 
  166  kubectl expose deploy helloworld-deployment --type=NodePort
  167  kubectl  get svc 
  168  kubectl expose deploy helloworld-deployment --type=NodePort --kubeconfig=/root/eks-cfg 
  169  kubectl expose deploy helloworld-deployment --type=LoadBalancer --kubeconfig=/root/eks-cfg 
  170  kubectl get svc  --kubeconfig=/root/eks-cfg 
  171  kubectl edit svc helloworld-deployment  --kubeconfig=/root/eks-cfg 
  172  kubectl get svc  --kubeconfig=/root/eks-cfg 
  173  kubectl  describe deploy helloworld-deployment
  174  kubectl set image deploy helloworld-deployment k8s-demo=amitvashist7/k8s-tiny-web:2
  175  kubectl scale --replicas=10 deploy helloworld-deployment
  176  kubectl  describe deploy helloworld-deployment
  177  kubectl set image deploy helloworld-deployment k8s-demo=amitvashist7/k8s-tiny-web:3
  178  kubectl rollout history deploy helloworld-deployment
  179  kubectl rollout history deploy helloworld-deployment --revision=1 
  180  kubectl rollout history deploy helloworld-deployment --revision=2
  181  kubectl rollout history deploy helloworld-deployment --revision=3
  182  kubectl  get pods 
  183  kubectl rollout status  deploy helloworld-deployment --revision=3
  184  kubectl set image deploy helloworld-deployment k8s-demo=amitvashist7/k8s-tiny-web:4
  185  kubectl rollout status  deploy helloworld-deployment --revision=3
  186  kubectl rollout status  deploy helloworld-deployment 
  187  ls
  188  cp -rf helloworld.yaml helloworld-u1.yaml 
  189  kubectl rollout history deploy helloworld-deployment 
  190  kubectl rollout status  deploy helloworld-deployment --revision=4
  191  kubectl rollout history deploy helloworld-deployment --revision=4
  192  vim helloworld-u1.yaml 
  193  kubectl apply -f helloworld-u1.yaml 
  194  kubectl rollout history deploy helloworld-deployment 
  195  kubectl rollout undo deploy helloworld-deployment 
  196  kubectl rollout history deploy helloworld-deployment 
  197  kubectl rollout undo deploy helloworld-deployment 
  198  kubectl rollout history deploy helloworld-deployment 
  199  kubectl rollout undo deploy helloworld-deployment --to-revision=1
  200  kubectl rollout history deploy helloworld-deployment 
  201  kubectl rollout history deploy helloworld-deployment --revision=8
  202  kubectl set image deploy helloworld-deployment k8s-demo=amitvashist7/k8s-tiny-web --record 
  203  kubectl set image deploy helloworld-deployment k8s-demo=amitvashist7/k8s-tiny-web:2 --record 
  204  kubectl set image deploy helloworld-deployment k8s-demo=amitvashist7/k8s-tiny-web:3 --record 
  205  kubectl set image deploy helloworld-deployment k8s-demo=amitvashist7/k8s-tiny-web:4 --record 
  206  kubectl rollout history deploy helloworld-deployment 
  207  ls
  208  history > README.md
```
