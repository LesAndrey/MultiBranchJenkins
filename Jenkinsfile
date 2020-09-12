library identifier: 'JenkinsLib@master', retriever: modernSCM(
  [$class: 'GitSCMSource',
   remote: 'https://github.com/LesAndrey/JenkinsLib.git'])

String CronExpr = timeTrigger(currentBuild.getNumber())

pipeline {
  agent any
  triggers {
    cron(CronExpr)
  }
  stages {
    stage('Even Stage') {
      steps {
        echo 'The build number is even'
      }
    }
  }
}
