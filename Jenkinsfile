pipeline {
    agent any

    tools {
        maven 'maven-3.9'
    }

    stages {

        stage("build-jar") {
            steps {
                script {
                    echo "building the application..."
                    sh 'mvn package'
                                        
                }
            }
        }

       stage("build image") {
            steps {
                script {
                    echo "building the docker image..."
                    withCredentials([usernamePassword(credentialsId: 'dockerhub', passwordVariable: 'PASS', usernameVariable: 'USER')]) {
                        sh 'docker build -t psegynola/philmay:4.0 .'
                        sh 'echo $PASS | docker login -u ${USER} --password-stdin'
                        sh 'docker push psegynola/philmay:4.0'
                    }
                }
            }
        } 
        
        stage("deploy") {
            steps {
                script {
                    echo "deploying the application..."

                }
            }
        }

        stage("philip") {
            steps {
                script {
                    echo "philiping the application..."

                }
            }
        }
        stage("mayowa") {
            steps {
                script {
                    echo "mayowaing the application..."

                }
            }
        }
        stage("lana") {
            steps {
                script {
                    echo "lanaing the application..."

                }
            }
        }
        stage("lani") {
            steps {
                script {
                    echo "laniing the application..."

                }
            }
        }
        stage("loni") {
            steps {
                script {
                    echo "loniing the application..."

                }
            }
        }
    }
}
