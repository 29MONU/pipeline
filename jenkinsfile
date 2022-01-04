pipeline
  {
    agent any
    stages {
            stage('BUILD') {
                    steps {
                            sh '''
                                    #!/bin/bash
                                    echo "This is first build"
                                 '''
                              }
                             }
              stage('TEST1') {
                    steps {
                            sh 'echo "first test stage in jenkinsfile"'
                            }
                           }
              stage('TEST2') {
                    steps {
                            sh 'echo "second test stage in jenkinsfile"'
                            }
                            }
               stage('DEPLOY') {
                      steps {
                      sh 'echo "final DEPLOY stage in jenkkinsfile"'
                      }
                      }
               }
        }
