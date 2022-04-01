```
714  cd 13-ConfigMap/
  715  ls
  716  cat nginx-deploy.yaml
  717  kubectl  run hello-ngnix --image=nginx:1.11 --port=80
  718  kubectl  get pods
  719  kubectl  expose pod hello-ngnix --type=NodePort
  720  kubectl  get pods,svc
  721  ls
  722  cat reverseproxy.conf
  723  kubectl create configmap nginx-config --from-file=reverseproxy.conf --dry-run
  724  kubectl create configmap nginx-config --from-file=reverseproxy.conf --dry-run -o yaml
  725  kubectl create configmap nginx-config --from-file=reverseproxy.conf --dry-run -o yaml > 01-ConfigMap.yaml
  726  ls
  727  mv nginx-deploy.yaml 02-nginx-deploy.yaml
  728  mv nginx-svc.yaml 03-nginx-svc.yaml
  729  ls
  730  kubectl apply -f 01-ConfigMap.yaml
  731  kubectl  get configmap
  732  kubectl describe configmap nginx-config
  733  ls
  734  vim 02-nginx-deploy.yaml
  735  ls
  736  kubectl  apply -f 02-nginx-deploy.yaml
  737  kubectl  get pods
  738  ld
  739  ls
  740  cat 03-nginx-svc.yaml
  741  kubectl apply -f 03-nginx-svc.yaml
  742  kubectl  get pods,svc
  743  kubectl  get pods
  744  kubectl exec -it helloworld-nginx -c nginx -- bash
  745  ls
  746  cd ..
  747  ls
  748  kubectl  delete -f 13-ConfigMap/
  749  ls
  750  cd ..
  751  git add . ; git commit -m "13-ConfigMap" ; git push
```
