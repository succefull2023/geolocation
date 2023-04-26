pipeline {
    agent any
    tools {
  maven 'M2_HOME'
}
    triggers {
  pollSCM '* * * * *'
}

    stages {
        stage('maven package') {
            steps {
                sh 'mwn clean'
                sh 'mwn install'
                sh 'mwn package'
            }
        }
              stage('test') {
            steps {
                sh 'mvn test'
        
            }
        }

              stage('deploy') {
            steps {
                echo 'deploy'
                
            }
        }
    }
}