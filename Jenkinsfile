pipeline {

agent any

stages {

stage('Checkout') {
steps {
echo "Pulling source code...."
checkout scm
}
}


stage('Build') {
steps {
echo "Building the application.."
}
}

stage('Test') {
steps {
echo "Running unit and integration testing .."
}
}

stage('packing') {
steps {
echo "packing artifact like Docker Image .."
}
}
}
}

