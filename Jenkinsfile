pipeline {
  agent {
    label 'master'
  }
  stages{
    stage('build'){
      steps {
      sh 'apk add perl bash'
      sh 'perl -c program.pl'
      }
    }
    stage('test'){
      steps {
      sh 'bash test.sh'
      }
    }
   }
}
