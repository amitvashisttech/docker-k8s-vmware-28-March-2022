    1  ls
    2  cd 
    3  echo "amitvashist7@outlook.com" > /root/username.txt 
    4  echo "Password@432!" > /root/password.txt 
    5  ls
    6  cat username.txt 
    7  cat password.txt 
    8  kubectl create secret --help
    9  kubectl create secret generic --help
   10  kubectl create secret generic my-secret --from-file=/root/username.txt --from-file=/root/password.txt 
   11  kubectl get secrets 
   12  kubectl describe secrets my-secret
   13  kubectl edit secrets my-secret
   14  cd - 
   15  ls
   16  vim 01-Secrets.yaml
   17  ls
   18  vim 02-deployment.yaml
   19  ls
   20  kubectl get secrets 
   21  kubectl  apply -f 01-Secrets.yaml 
   22  kubectl get secrets 
   23  ls
   24  cat 02-deployment.yaml 
   25  kubectl get secrets 
   26  vim 02-deployment.yaml 
   27  ls
   28  kubectl  apply -f 02-deployment.yaml 
   29  kubectl  get pods 
   30  kubectl describe pod helloworld-deployment-58cb57874f-ck54q
   31  kubectl exec -it helloworld-deployment-58cb57874f-ck54q  -- /bin/sh 
   32  ls
   33  history 
   34  ls
   35  history > README.md 
