# SciGraph-docker-monarch
Build two Docker images with the monarch configs. Uses master HEAD from the SciGraph github repo.

Need to have docker installed in order to run the build.

mvn package to generate the images.


Load the graph:

docker run -v /tmp/monarchGraph:/monarchGraph scigraph-load-monarch

Run the services:

docker run -v /tmp/monarchGraph:/monarchGraph -p 9000:9000 scigraph-services-monarch
