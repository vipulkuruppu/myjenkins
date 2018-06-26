@Library('uob-shared') _
import uob.shared.pom.*
//import uob.shared.common.*

pipeline {
    agent any
    environment{
        def pomversion = getPOMVersion(branchtype: 'Core', pomfile: 'pom.xml')
        def pomversionnew = getPOMVersionFromTester('Core', 'pom.xml')
        //script{
        //    def pr = new POMTester()
        //    def pomversionnew = pr.readVersion('Core', 'pom.xml')
        //}
    }
    stages{
        stage('pom-read'){
            steps{
                echo "${env.pomversion}"
            }
        }
        stage('scripted-pom-read'){
            steps{
                echo "${env.pomversionnew}"
            }
        }
        stage('say-message'){
            steps{
                script{
                    say.hello('Vipul')
                    say.bye('Vipul')
                }
            }
        }
        stage('say-from-script'){
            steps{
                script{
                    say.hellofromsh('Vipul', 'test')
                }
            }
        }
    }
}
