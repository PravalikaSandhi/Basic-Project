pipeline {
        agent any 
                stages {
                        stage('one') {
                                steps {
                                        echo 'Hi, this is pravalika from github'
                                }
                        }
                        stage('two') {
                                steps { 
                                        input('do you want to proceed?')
                                }
                        }
                        stage('three') {
                                when {
                                         not {
                                                  branch "master"
                                         }
                                }
                                steps {
                                         echo "Hello"
                                }
                        }
                        stage('four') {
                                        parallel {
                                              stage('unit test') {
                                                                 steps {
                                                                       echo "running the unit test..."
                                                                 }
                                              }
                                              stage('integration test') {
                                                                 agent {
                                                                       docker {
                                                                                reusenode false
                                                                                image 'ubuntu'
                                                                       }
                                                                 }
                                                                 steps {
                                                                        echo 'running the integration test...'
                                                                 }
                                               }
                                         }
}
}
}
