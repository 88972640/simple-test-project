pipeline {
    agent any

    tools {
        maven "MAVEN_HOME"
       }
    stages {
        stage('build'){
            steps{
                echo "hello harsha"
            }
        }
        stage('test') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            
            }
        }
     }
    post {
       always {
          junit(
        allowEmptyResults: true,
        testResults: '*/test-reports/.xml'
      )
      }
   } 
}
