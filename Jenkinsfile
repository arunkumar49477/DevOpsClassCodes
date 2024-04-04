pipeline {
    agent any
  stages {
      stage('Clonerepo from github ') {
         steps {
            git 'https://github.com/bhasker-manikyala/DevOpsClassCodes.git'
         }
      }
      stage('Compile the code') {
         steps {
            sh 'mvn compile'
         }
      }
     stage('Build') {
        steps {
            sh 'mvn clean package'
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
      stage('Package') {
    steps {
        sh 'mvn package'
    }
}
 //     stage('Deploy') {
  //  steps {
        // Example: Deploy to Nexus repository
    //    sh 'mvn deploy'
    //}
//}
  }
}
