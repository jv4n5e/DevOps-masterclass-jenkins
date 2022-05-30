pipeline {
      agent any
      stages {
            stage('Build app') {
                  steps {
                        sh 'mvn clean package'
                  }
            }
            post {
                success {
                    echo "mvn clean package successful. Now, archiving the artifacts..."
                    archiveArtifacts artifacts: '**/*.war'
                }
            }
      }
}