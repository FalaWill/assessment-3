pipeline {
        agent any
                stages {
                        stage ('one') {
                                  steps {
                                          echo 'Hi, this is William'
                                  }
                        }

                        stage ('two') {
                                  steps {
                                          input('Do you want to proceed?')

                                  }
                        }

                        stage ('three') {
                                 when{
                                        not {
                                                branch "master"
                                        }

                                 }
                                 steps {
                                          echo "Hello"
                                 }
                        }

                        stage ('four') {
                                        parallel {
                                          stage ('Unit Test'){
                                                    steps {
                                                          echo 'Running the unit test...'
                                                          }
                                                              }
                                          }

                                          }




                        }

              }
}
