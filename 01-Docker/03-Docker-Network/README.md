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
