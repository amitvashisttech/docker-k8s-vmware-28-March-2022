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

```
599  kubectl  get pods
  600  kubectl scale --replicas=1 deploy toleration-deployment
  601  kubectl scale --replicas=1 deploy helloworld-deployment
  602  ls
  603  kubectl  get pods
  604  cd 02-K8s/10-Taint-and-Toleration/
  605  ls
  606  vim 03-helloworld-toleration-2.yaml
  607  kubectl apply -f 03-helloworld-toleration-2.yaml
  608  kubectl  get pods -o wide
  609  kubectl taint nodes worker1 example2=example2-key:NoExecute
  610  kubectl describe nodes | grep -i taint
  611  kubectl describe nodes worker1 | grep -i taint
  612  kubectl describe nodes worker1 | grep -iA2 taint
  613  kubectl  get pods -o wide
  614  ls
  615  vim 04-helloworld-toleration-3.yaml
  616  kubectl  apply -f 04-helloworld-toleration-3.yaml
  617  kubectl  get pods -o wide
  618  kubectl delete -f ../10-Taint-and-Toleration/
  619  kubectl describe nodes worker1 | grep -iA2 taint
  620  kubectl taint nodes worker1 example2-
  621  kubectl taint nodes worker1 example-
  622  kubectl describe nodes  | grep -iA2 taint
  623  kubectl taint nodes worker2 app-
  624  kubectl describe nodes  | grep -iA2 taint
```
