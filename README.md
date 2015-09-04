docker for glassfish 4.1

to build this image I recomment the following comands

docker build --no-cache=true -f dockerfile-glassfish4-java8 -t skuarch/glassfish4-java8 .

docker run --name glassfish4-java8 -i -t -p 8080:8080 -p 4848:4848 -c 4 --net=host -m 4096M  -v /home/skuarch/docker/glassfish4-java8/glassfish4/:/home/skuarch/docker/glassfish4-java8/glassfish4/ skuarch/glassfish4-java8

options -c and -m are optional
