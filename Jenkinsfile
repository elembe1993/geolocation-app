pipeline {
    agent any
               tools {
  maven 'M2_HOME'
}

    triggers {
  pollSCM ('* * * * *')
}


    stages {
        stage('maven package') {
 
            steps {
                sh 'mvn clean'
                sh 'install'
                sh 'package'
                echo 'Hello maven command'
            }
        }
         stage('test') {
            steps {
                sh 'test'
                echo 'Hello testing'
            }
        }
         stage('check') {
            steps {
                echo 'Hello check'
            }
        }
         stage('deploy') {
            steps {
                echo 'Hello deploy my changes'
            }
        }
    }
}
