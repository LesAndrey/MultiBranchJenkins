library identifier: 'JenkinsLib@master', retriever: modernSCM(
  [$class: 'GitSCMSource',
   remote: 'https://github.com/LesAndrey/JenkinsLib.git'])

// String timeTriggerJenkinsfile(int buildNumber) {
//     String cronExpr=timeTriggerExpr(buildNumber)
//     println cronExpr
//     return cronExpr
// }

// String CronExpr = timeTriggerJenkinsfile(currentBuild.getNumber())
// println CronExpr

pipeline {
  agent any
  // triggers {
  //   cron(CronExpr)
  // }
  stages {
    stage('Even Stage') {
      steps {
        echo 'The build number is even'
        println timeTriggerExpr(currentBuild.getNumber())
      }
    }
  }
}
