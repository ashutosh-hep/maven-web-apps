pipeline {
    agent any
    stages {
        stage("start"){
            steps {
                deleteDir()
            }
        }
        stage("clone repo"){
            steps {
                sh "git clone https://github.com/ashutosh-hep/maven-web-apps.git"
            }
        }
        stage("build"){
            steps {
                dir("maven-web-apps"){
                    sh ''' 
                    cd spring-boot-demo
                    mvn -Denforcer.skip=true clean install
                    '''
                }
            }
        }
    }
}