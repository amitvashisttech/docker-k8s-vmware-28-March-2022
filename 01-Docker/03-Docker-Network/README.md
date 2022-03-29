```
    1  cd 

    2  docker ps -a 
    3  docker images 
    4  docker run -d --name test-nw-1 myapache:v3 
    5  docker ps 
    6  docker inspect test-nw-1
    7  docker run -d --name test-nw-2 myapache:v3 
    8  docker inspect test-nw-2
    9  docker network ls 
   10  docker network inspect 80324d018502
   11  ip addr 
   12  route -n 
   13  docker network inspect 80324d018502
   14  docker run -d --name test-nw-3 myapache:v3 
   15  docker run -d --name test-nw-4 myapache:v3 
   16  docker network inspect 80324d018502
   17  docker ps 
   18  docker stop test-nw-2
   19  docker ps 
   20  docker inspect test-nw-2
   21  docker network inspect 80324d018502
   22  docker run -d --name test-nw-5 myapache:v3 
   23  docker network inspect 80324d018502
   24  docker start test-nw-2
   25  docker network inspect 80324d018502
   26  curl 172.17.0.6 
   27  route -n 
   28  ip addr 
   29  curl 172.17.0.6 
   30  docker ps 
   31  docker run -d --name test-nw-6 -p 8080:80 myapache:v3 
   32  docker ps 
   33  netstat -tulnp 
   34  systemctl status docker
   35  curl 172.17.0.7
   36  curl localhost
   37  netstat -tulnp 
   38  curl localhost:8080
   39  systemctl status docker
   40  ls
   41  docker run -d --name test-nw-7 -p 8081:80 myapache:v2 
   42  docker run -d --name test-nw-7 -p 8082:80 myapache:v1
   43  docker run -d --name test-nw-8 -p 8082:80 myapache:v1
   44  docker ps 
   45  systemctl status docker
   46  docker ps 
   47  netstat -tulnp 
   48  docker run -d --name test-nw-9 -P myapache:v1
   49  docker ps 
   50  docker inspect f298b461548e
   51  docker inspect f298b461548e | grep -i 80 
   52  ls
   53  cd docker-k8s-vmware-28-March-2022/
   54  ls
   55  cd 01-Docker/02-DockerVolumes/
   56  ls
   57  cd ..
   58  ls
   59  cd 01-DockerFile/
   60  ls
   61  cd apache/
   62  ls
   63  cp -rf v2 v4 
   64  ls
   65  cd v4/
   66  ls
   67  vim Dockerfile 
   68  docker images 
   69  docker build -t myapache:v4 . 
   70  docker ps 
   71  curl 172.17.0.3
   72  curl 172.17.0.3:80
   73  docker run -d --name test-nw-2-1 -P myapache:v4
   74  docker ps 
   75  docker kill test-nw-2-1
   76  docker rm test-nw-2-1
   77  docker run -d --name test-nw-2-1 myapache:v4
   78  docker ps 
   79  docker inspect test-nw-2-1
   80  telent 172.17.0.11 
   81  telnet 172.17.0.11 
   82  docker ps 
   83  telnet 172.17.0.11 80 
   84  ls
   85  vim Dockerfile 
   86  docker build -t myapache:v5 . 
   87  docker run -d --name test-nw-2-2 myapache:v5
   88  docker ps 
   89  telnet 172.17.0.12 80 
   90  telnet 172.17.0.12 3306 
   91  docker ps 
   92  docker run -d --name test-nw-2-3 -P myapache:v4 
   93  docker ps 
   94  docker run -d --name test-nw-2-4 -P myapache:v4 
   95  docker run -d --name test-nw-2-5 -P myapache:v4 
   96  docker ps 
   97  docker run -d --name test-nw-2-6 -P myapache:v5 
   98  docker ps 
   99  ls
  100  cd ..
  101  ls
  102  cd ..
  103  ls
  104  cd ..
  105  ls
  106  history 03-Docker-Network/README.md 
  107  history > 03-Docker-Network/README.md 
```




```
    1  ls
    2  cd docker-k8s-vmware-28-March-2022/
    3  ls
    4  docker ps 
    5  docker images 
    6  docker run -d --name test-1 -p 8080:80 myapache:v3 
    7  docker ps 
    8  docker run -d --name test-2 -P  myapache:v3 
    9  docker ps 
   10  docker run -d --name test-3 -P  myapache:v4 
   11  docker ps 
   12  netstat -tunlp
   13  systemctl status docker 
   14  docker ps 
   15  grep -i format 00-History/Day1_History.txt 
   16  docker inspect --format '{{.Name}} {{.State.Running}} {{.NetworkSettings.IPAddress}}' $(docker ps -aq)
   17  docker network ls 
   18  docker network inspect 52c80a851654
   19  docker ps 
   20  ls
   21  cd 01-Docker/
   22  ls
   23  cd 01-DockerFile/
   24  ls
   25  mkdir python 
   26  ls
   27  cd python/
   28  ls
   29  vim app.
   30  vim app.py 
   31  ls
   32  vim req.txt 
   33  ls
   34  vim Dockerfile
   35  ls
   36  docker build -t mypyapp:v1 . 
   37  docker ps 
   38  docker images 
   39  docker run -d --name py-app-1 -P  mypyapp:v1 
   40  docker ps 
   41  docker images 
   42  docker ps 
   43  docker run -d --name py-app-2 -P  mypyapp:v1 
   44  docker ps 
   45  ls
   46  cd 
   47  ls
   48  docker network ls 
   49  docker ps 
   50  docker kill 151fc93a313e df7e7b85c2dc 19b18cca9344 768999ff9d68
   51  docker ps 
   52  docker rm 151fc93a313e df7e7b85c2dc 19b18cca9344 768999ff9d68
   53  docker network ls 
   54  docker network create my-net 
   55  docker network ls 
   56  docker network inspect my-net
   57  docker network ls 
   58  docker run -d --name py-app-3 -P --network my-net mypyapp:v1 
   59  docker ps 
   60  docker inspect --format '{{.Name}} {{.State.Running}} {{.NetworkSettings.IPAddress}}' $(docker ps -aq)
   61  docker inspect py-app-3
   62  curl 172.18.0.2:5001
   63  docker network ls 
   64  docker network inspect my-net
   65  ip addr 
   66  docker network create --help
   67  docker network create --driver=bridge --subnet=172.28.0.0/16 --ip-range=172.28.5.1/24 --gateway=172.28.5.254 mybr0 
   68  docker network ls 
   69  docker network inspect mybr0   
   70  docker run -d --name py-app-4 -P --network mybr0 mypyapp:v1 
   71  docker run -d --name py-app-5 -P --network mybr0 mypyapp:v1 
   72  docker ps 
   73  docker network inspect mybr0   
   74  ip addr 
   75  ls
   76  docker kill $(docker ps -qa) 
   77  docker rm $(docker ps -qa) 
   78  ls
   79  docker network ls 
   80  docker network rm my-net 
   81  docker network ls 
   82  ls
   83  cd docker-k8s-vmware-28-March-2022/
   84  ls
   85  cd 01-Docker/
   86  ls
   87  cd 03-Docker-Network/
   88  ls
   89  history 
   90  ls
   91  >> README.md 
   92  vim README.md 
   93  history >> README.md 
```

```
  100  git add . ; git commit -m "Network" ; git push 
  101  docker network 
  102  docker network ls 
  103  docker ps -a 
  104  docker run -itd --name net-tools ubuntu:16.04
  179  docker exec -it net-tools apt-get update
  182  docker exec -it net-tools apt-get install net-tools -y
  105  docker ps 
  106  docker commit -p -m "Network Tools Installed" net-tools ubuntu-nettool:v1
  107  docker images 
  108  docker kill $(docker ps -qa) 
  109  docker rm  $(docker ps -qa) 
  110  docker network ls 
  111  docker run -d --name test-1 -P --network mybr0 ubuntu-nettools:v1 
  112  docker images 
  113  docker run -d --name test-2 -P --network mybr0 ubuntu-nettool:v1 
  114  docker ps 
  115  docker run -itd --name test-3 -P --network mybr0 ubuntu-nettool:v1 
  116  docker ps 
  117  docker inspect test-3
  118  docker ps 
  119  docker exec -it test-3 ifconfig 
  120  docker exec -it test-3 route -n 
  121  docker network ls 
  122  docker run -itd --name test-4 -P --network none ubuntu-nettool:v1 
  123  docker ps 
  124  docker inspect test-4
  125  docker exec -it test-4 ifconfig 
  126  docker exec -it test-3 ifconfig 
  127  docker ps 
  128  docker run -itd --name test-5 -P --network host ubuntu-nettool:v1 
  129  docker ps 
  130  docker exec -it test-5 ifconfig 
  131  docker ps 
  132  docker images 
  133  docker run -itd --name test-6  --network host myapache:v4 
  134  docker ps 
  135  docker inspect test-6
  136  docker ps 
  137  netstat -tulnp 
  138  docker run -itd --name test-7  -P myapache:v4 
  139  netstat -tulnp 
  140  docker ps 
  141  docker inspect 045d6c449170
  142  docker inspect 045d6c449170 | grep -i expose 
  143  docker inspect 045d6c449170 | grep -iA5 expose 
  144  netstat -tunlp 
  145  docker ps 
  146  docker run -d myapache:v2 
  147  docker ps 
  148  docker inspect 76124908a38a
  149  telnet 172.17.0.3 5001 
  150  docker images 
  151  sl
  152  ls
  153  cd 01-Docker/
  154  ls
  155  cd 01-DockerFile/
  156  ls
  157  cd python/
  158  ls
  159  cat app.py 
  160  vim app.py 
  161  docker build -t mypyapp:v2 . 
  162  docker run -d mypyapp:v2 
  163  docker ps 
  164  docker run -d  --network host mypyapp:v2 
  165  docker ps 
  166  netstat -tulnp 
  167  curl localhost:9001
  168  curl localhost:5001
  169  ls
  170  cd ..
  171  ls
  172  cd ..
  173  ls
  174  cd 03-Docker-Network/
  175  ls
  176  history >> README.md 
```
