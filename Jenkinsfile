node {
    stage('Build') { // for display purposes
        export DOCKERID=bfulle200
        docker image build --tag $DOCKERID/cw2:1.0 .
        docker container stop cw2
        docker container rm cw2
        docker container run --detach --publish 80:80 --name cw2 $DOCKERID/cw2:1.0
        docker exec --workdir /tmp cw2 ps -ef
        docker login --username=bfulle200 --password=LvQ1okV^59y8
        docker image push $DOCKERID/cw2:1.0
    }
}
