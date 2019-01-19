pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
      logstash {
        build 'Build'
        echo 'build'
        }
      }
    }
    stage('Selenium') {
        steps {
        logstash {
            build 'selenium1.0'
            echo 'selenium'
         }
        }
    }
    stage('Cucumber') {
          steps {
          logstash {
            build 'cucumber'
            echo 'cucumber'
          }
         }
    }
    stage('smartbear') {
      steps {
      logstash {
        build 'smartbear'
        echo 'smartbear'
      }
     }
    }
    stage('Sonarqube') {
          steps {
          logstash {
            build 'sonarcube'
            echo 'sonarqube'
          }
         }
        }
    stage('xldeploy') {
       steps {
       logstash {
         build 'awsupload'
         echo 'aws upload'
       }
      }
    }
  }

 post {
   always {
      logstashSend failBuild: true, maxLines: 1000
      }

  }

}
