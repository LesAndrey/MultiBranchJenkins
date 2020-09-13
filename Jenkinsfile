library identifier: 'JenkinsLib@master', retriever: modernSCM(
  [$class: 'GitSCMSource',
   remote: 'https://github.com/LesAndrey/JenkinsLib.git'])

String cron=timeTriggerExpr

pipeline {
  agent any
  triggers {
    cron(cron)
  }
  stages {
    stage('Even Stage') {
      steps {
        echo 'The build number is even'
      }
    }
  }
}
