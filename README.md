docker for glassfish 4.1

to build this image I recomment the following comands

docker build --no-cache=true -f dockerfile-glassfish4-java8 -t skuarch/glassfish4-java8 .

docker run --name glassfish4-java8 -i -t -p 8080:8080 -p 4848:4848 -c 4 --net=host -m 4096M  -v /home/skuarch/docker/glassfish4-java8/glassfish4/:/home/skuarch/docker/glassfish4-java8/glassfish4/ skuarch/glassfish4-java8

options -c and -m are optional if you prefer download the jdk from oracle is posible with this command

#curl -L -O -H "Cookie: oraclelicense=accept-securebackup-cookie" -k "https://edelivery.oracle.com/otn-pub/java/jdk/8u60-b27/jdk-8u60-linux-x64.tar.gz"
