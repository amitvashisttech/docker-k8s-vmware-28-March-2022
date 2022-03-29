```
 194  docker images
  195  docker push mypyapp:v1
  196  docker login
  197  docker push mypyapp:v1
  198  docker images
  199  docker tag a7cf9e245cf4 amitvashist7/mypyapp-vmware-29-mar-2022:v1
  200  docker tag a7cf9e245cf4 amitvashist7/mypyapp-vmware-29-mar-2022:latest
  201  docker images
  202  docker push amitvashist7/mypyapp-vmware-29-mar-2022:v1
  203  docker push amitvashist7/mypyapp-vmware-29-mar-2022:latest
  204  docker kill $(docker ps -qa)
  205  docker rm $(docker ps -qa)
  206  docker images
  207  docker rmi amitvashist7/mypyapp-vmware-29-mar-2022:latest
  208  docker rmi amitvashist7/mypyapp-vmware-29-mar-2022:v1
  209  docker images
  210  docker logout
  211  docker pull amitvashist7/mypyapp-vmware-29-mar-2022
```
