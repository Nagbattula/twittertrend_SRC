def registry = 'https://valaxy02.jfrog.io'
def imageName = 'valaxy02.jfrog.io/valaxy-docker/ttrend'
def version   = '2.0.3'
pipeline{
    agent {
        node {
            label "maven-agent"
        }
    }
    environment {
        PATH = "/opt/apache-maven-3.9.1/bin:$PATH"
    }
    stages {
        stage('build') {
            steps{
                echo "------------ build started ---------"
                sh 'mvn clean deploy -Dmaven.test.skip=true'
                echo "------------ build completed ---------"
            }
        }
    }
}