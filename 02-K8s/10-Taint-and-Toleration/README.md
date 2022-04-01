```
 563  mkdir 10-Taint-and-Toleration
  564  ls
  565  cd 10-Taint-and-Toleration/
  566  ls
  567  kubectl  get nodes
  568  kubectl describe nodes master | grep -i taint
  569  kubectl describe nodes | grep -i taint
  570  kubectl taint nodes worker2 app=myapp:NoSchedule
  571  kubectl describe nodes | grep -i taint
  572  ls
  573  vim 01-helloworld.yaml
  574  ls
  575  cat 01-helloworld.yaml
  576  kubectl  apply -f 01-helloworld.yaml
  577  kubectl  get pods -o wide
  578  vim 02-helloworld-toleration.yaml
  579  kubectl  apply -f 02-helloworld-toleration.yaml
  580  kubectl  get pods -o wide
  581  kubectl taint nodes worker1 example=amit:NoSchedule
  582  kubectl describe nodes | grep -i taint
  583  kubectl  get pods -o wide
  584  kubectl scale --replicas=8 deploy helloworld-deployment
  585  kubectl  get pods -o wide
  586  kubectl scale --replicas=8 deploy toleration-deployment
  587  kubectl  get pods -o wide
  588  kubectl scale --replicas=3 deploy toleration-deployment
```
