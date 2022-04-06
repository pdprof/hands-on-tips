# Liberty and Java PD Hands-on tips

## Standalone java program 

Test standalone java program with various java versions and vendors
```
Main class in jar file located at docker-host:/work/pdprof.jar.
docker run --rm -v `pwd`:/work ibmjava java -jar /work/pdprof.jar <program args>

Main class located at docker-host:/work directory.
docker run --rm -v `pwd`:/work ibmjava java -classpath /work Main <program args>
```

You can change "ibmjava" word to the other java docker image.


## tWAS docker 

I put a Dockerfile under was90 directory to use tWAS docker image in this repositry.
Edit was version tag to the latest which is available from the public docker repository.
```
# After pull this repository
cd was90

# Edit WAS version
vi Dockerfile

# Edit port number to use
vi virtual-host.py
vi start.sh

# Build
docker build -t was90 .

# Start
./start.sh
```
