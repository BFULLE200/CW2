node {
    stage('Build') { // for display purposes
        sh 'docker image build --tag bfulle200/cw2:1.0 .'
        sh 'docker container stop cw2'
        sh 'docker container rm cw2'
        sh 'docker container run --detach --publish 80:80 --name cw2 bfulle200/cw2:1.0'
        sh 'docker exec --workdir /tmp cw2 ps -ef'
        sh 'docker login --username=bfulle200 --password=LvQ1okV^59y8'
        sh 'docker image push bfulle200/cw2:1.0'
    }
}
