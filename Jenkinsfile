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
                        
}
}
