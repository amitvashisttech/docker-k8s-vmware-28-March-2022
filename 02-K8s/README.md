```
133  kubectl  get pods -n kube-system
  134  cd /etc/kubernetes/
  135  ls
  136  cat admin.conf
  137  ls
  138  cd manifests/
  139  ls
  140  cat etcd.yaml
  141  ls
  142  vim kube-apiserver.yaml
  143  cd
  144  kubectl cluster-info
  145  kubectl  get pods
  146  kubectl cluster-info
  147  kubectl cluster-info dump
  148  kubectl  get pods
  149  kubectl  logs mypywebapp
  150  kubectl  version
  151  kubectl api-versions
  152  ls
  153  cat docker-k8s-vmware-28-March-2022/02-K8s/01-First-App/nginx-pod.yaml
  154  kubectl api-versions
  155  kubectl api-resources
  156  curl https://172.31.0.100:6443 -k
  157  kubectl proxy --address='172.31.0.100' --port=8080 --accept-hosts='.' --accept-paths='.' &
  158  kubectl  get pods
  159  kubectl  get pods -o wide
  160  kubectl  describe pods  mypywebapp
  161  cat .kube/config
  162  kubectl config view
  163  kubectl config get-contexts
  164  ls
  165  cd docker-k8s-vmware-28-March-2022/
```
