library identifier: 'JenkinsLib@master', retriever: modernSCM(
  [$class: 'GitSCMSource',
   remote: 'https://github.com/LesAndrey/JenkinsLib.git'])

def timeTriggerJenkinsfile(int buildNumber) {
    myTimeTrigger(buildNumber)
}

String CronExpr = timeTriggerJenkinsfile(currentBuild.getNumber())

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
