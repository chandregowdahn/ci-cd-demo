pipeline {

agent {
docker {
image 'node:20'
}
}

stages {

stage('Checkout') {
steps {
checkout scm
}
}

stage('Install Dependencies') {
steps {
sh 'npm install'
}
}

stage('Run Tests') {
steps {
sh 'npm test'
}
}

stage('Build') {
steps {
sh 'npm run build'
}
}

stage('Package Artifact') {
steps {
sh 'tar -czf artifact.tar.gz *'
archiveArtifacts artifacts: 'artifact.tar.gz'
}
}
}
}

