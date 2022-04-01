```
 954  mkdir 16-Helm-Custom-Charts
  955  cd 16-Helm-Custom-Charts/
  956  ls
  957  helm create mychart
  958  ls
  959  cd mychart/
  960  ls
  961  cat values.yaml
  962  ls
  963  ls -ltr templates/
  964  vim templates/deployment.yaml
  965  ls
  966  vim values.yaml
  967  cd ..
  968  ls
  969  vim mychart/values.yaml
  970  helm install mynginx mychart --dry-run
  971  helm install mynginx mychart
  972  kubectl  get deploy,rs,pod,svc
  973  ls
  974  cd ..
  975  ls
  976  cd 16-Helm-Custom-Charts/
  977  ls
  978  helm create mypyapp
  979  ls
  980  cd mypyapp/
  981  cd ..
  982  l
  983  ls
  984  vim mypyapp/values.yaml
  985  ls
  986  vim mypyapp/templates/deployment.yaml
  987  ls
  988  helm install my-py-webapp mypyapp --dry-run
  989  helm install my-py-webapp mypyapp
  990  kubectl  get deploy,rs,pod,svc
  991  \
  992  kubectl  get pods -o wide
  993  ls
  994  cd ..
  995  ls
  996  cd 16-Helm-Custom-Charts/
```
