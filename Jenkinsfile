library identifier: 'JenkinsLib@master', retriever: modernSCM(
  [$class: 'GitSCMSource',
   remote: 'https://github.com/LesAndrey/JenkinsLib.git'])

pipeline {
  agent any
  environment { 
        CRON_EXPR = '*/2 * * * 0-7'
  }
  triggers {
    cron(env.CRON_EXPR)
  }
  stages {
    stage('Even Stage') {
      steps {
        echo 'The build number is even'
      }
    }
  }
}
