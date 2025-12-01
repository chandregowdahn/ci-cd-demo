pipeline {

agent any

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
sh 'npx jest'
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

