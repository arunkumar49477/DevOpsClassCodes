pipeline {
    agent any
  stages {
      stage('Clonerepo from github') {
         steps {
            git 'https://github.com/bhasker-manikyala/DevOpsClassCodes.git'
         }
      }
      stage('Compile the code ') {
         steps {
            sh 'mvn compile'
         }
      }
      stage('CodeReview') {
         steps {
            sh 'mvn pmd:pmd'
         }
      }
      stage('UnitTesting') {
         steps {
            sh 'mvn test'
         }
      }

  }
}
