pipeline {
          agent any
          
          stages {
                  stage ("Clean up"){
                                     steps {
                                            deleteDir()
                                     }
                  }
                  stage ("Clone repo") {
                                        steps {
                                               sh "git clone https://github.com/alahammami2/sringboot_application.git"
                                        }
                  }
                  stage ("Generate backend image") {
                                                    steps {
                                                           dir ("sringboot_application"){
                                                                                         sh "avn clean install"
                                                                                         sh "docker build-t docexp1-spring."
                                                           }
                                                    }
                 }
                 stage ("Run docker compose") {
                                               steps {
                                                      dir("exp1-spring"){
                                                                         sh "docker compose up-d"
                                                      }
                                               }
                 }
          }
}
