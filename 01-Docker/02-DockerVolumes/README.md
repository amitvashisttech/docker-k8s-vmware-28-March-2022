```
    1  ls
    2  docker ps 
    3  docker kill $(docker ps -qa) 
    4  docker rm $(docker ps -qa) 
    5  ls
    6  mkdir 02-DockerVolumes 
    7  ls
    8  cd 02-DockerVolumes/
    9  ls
   10  cd ..
   11  ls
   12  docker volume ls 
   13  docker volume create my-vol 
   14  docker volume ls 
   15  docker volume inspect my-vol
   16  ls -ltr /var/lib/docker/volumes/
   17  ls -ltr /var/lib/docker/volumes/my-vol/_data/
   18  ls
   19  ls -ltr /var/lib/docker/volumes/my-vol/_data/
   20  docker volume ls 
   21  ls
   22  docker run -it --name vol-test-1 --mount source=my-vol,target=/app ubuntu
   23  ls
   24  docker ps 
   25  docker volume ls 
   26  docker inspect vol-test-1
   27  ls
   28  cat /var/lib/docker/volumes/my-vol/_data/hello.txt 
   29  hostname >> /var/lib/docker/volumes/my-vol/_data/hello.txt
   30  pwd >> /var/lib/docker/volumes/my-vol/_data/hello.txt
   31  date >> /var/lib/docker/volumes/my-vol/_data/hello.txt
   32  cat /var/lib/docker/volumes/my-vol/_data/hello.txt 
   33  ls
   34  docker ps 
   35  docker attach vol-test-1
   36  docker exec -it vol-test-1 cat /app/hello.txt
   37  docker ps 
   38  docker kill vol-test-1
   39  docker rm  vol-test-1
   40  docker ps -a 
   41  docker volume ls 
   42  docker run -it --name vol-test-2 --mount source=my-vol,target=/app busybox 
   43  docker volumes ls 
   44  docker volume ls 
   45  docker volume rm my-vol
   46  docker kill $(docker ps -qa) 
   47  docker volume rm my-vol
   48  docker rm $(docker ps -qa) 
   49  docker volume rm my-vol
   50  docker run --name alpha -it -v /var/www/amit ubuntu
   51  docker ps 
   52  docker inspect alpha
   53  ls
   54  cat /var/lib/docker/volumes/b07ed41faa46d81218a24a45e47e29862c0a0e39e3795f3e0fb064a6b142af1a/_data/abc.txt 
   55  docker volume ls 
   56  docker ps 
   57  pwd
   58  docker run --name beta -it -v /root/docker-k8s-vmware-28-March-2022:/var/www/amit ubuntu
   59  docker run --name beta-2 -it -v /root/docker-k8s-vmware-28-March-2022:/var/www/amit:ro ubuntu
   60  docker volume ls 
   61  docker inspect beta-2
   62  docker inspect beta
   63  docker inspect alpha
   64  sl
   65  ls
   66  docker ps 
   67  docker kill $(docker ps -qa) 
   68  docker rm $(docker ps -qa) 
   69  docker volume ls 
   70  docker run -itd --name data -v /var/www/html -v /var/log/amit -v /etc/amit -v /root/docker-k8s-vmware-28-March-2022:/myapp:ro busybox 
   71  docker ps 
   72  docker inspect data
   73  docker ps 
   74  docker attach data
   75  docker ps 
   76  docker images 
   77  docker run -d --name def-apache myapache:v3 
   78  curl 172.17.0.3
   79  docker run -d --name test-apache-1 --volumes-from data myapache:v3 
   80  docker run -d --name test-apache-2 --volumes-from data myapache:v3 
   81  docker run -d --name test-apache-3 --volumes-from data myapache:v3 
   82  docker inspect test-apache-1
   83  grep -i "format" 00-History/Day1_History.txt 
   84  docker inspect --format '{{.Name}} {{.State.Running}} {{.NetworkSettings.IPAddress}}' $(docker ps -aq)
   85  curl 172.17.0.6
   86  curl 172.17.0.5
   87  curl 172.17.0.4
   88  curl 172.17.0.3
   89  docker ps 
   90  docker inspect data
   91  echo "Hello Volumes" > /var/lib/docker/volumes/b271bd63c712aff2e30be03d4ec26854dafad1128b51a75c661622ac23c371c4/_data/index.html
   92  curl 172.17.0.3
   93  curl 172.17.0.4
   94  curl 172.17.0.5
   95  curl 172.17.0.6
   96  echo "<h1> Welcome to Data Container Volumes Demo </h1>" > /var/lib/docker/volumes/b271bd63c712aff2e30be03d4ec26854dafad1128b51a75c661622ac23c371c4/_data/index.html
   97  curl 172.17.0.6
   98  curl 172.17.0.5
   99  curl 172.17.0.4
  100  docker run -d --name test-apache-5 --volumes-from data myapache:v2
  101  curl 172.17.0.7
  102  docker kill $(docker ps -qa) 
  103  docker ps -a 
  104  docker rm $(docker ps -qa) 
  105  docker volumes ls 
  106  docker volume ls 
  107  docker volume ls -q
  108  docker volume rm $(docker volume ls -q) 
  109  ls
  110  cd 01-Docker/
  111  ls
  112  cd 02-DockerVolumes/
  113  ls
  114  history > README.md
```
