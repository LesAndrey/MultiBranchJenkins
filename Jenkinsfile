library identifier: 'JenkinsLib@master', retriever: modernSCM(
  [$class: 'GitSCMSource',
   remote: 'https://github.com/LesAndrey/JenkinsLib.git'])

def timeTriggerJenkinsfile(int buildNumber) {
    if (buildNumber % 2 == 0) {
        return '*/1 * * * 0-7'
    }else{
        return '*/2 * * * 0-7'
    }
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
