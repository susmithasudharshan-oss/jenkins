pipeline {
agent any
stages {
stage ('checkout') {
steps {
checkout scmGit(banches: [[name: '*/main']], extension: [], userRemoteconfigs: [[credentialsId: 'jnekinstoken', url: 'https://github.com/susmithasudharshan-oss/jenkins.git']]
}
}
}
}
