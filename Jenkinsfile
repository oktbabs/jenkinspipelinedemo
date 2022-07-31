pipeline {
    agent any
    stages {
        stage('Coding Stage') {
            steps {
                echo 'This is the Coding Stage'
            }
        }
        stage('Build') {
            steps {
                echo 'This is the Build Stage'
            }
        }
        stage('Testing') {
            steps {
                echo 'This is the Test Confirmation Stage'
            }
        }
        stage('Release') {
            steps {
                echo 'This is the release Confirmation Stage'
            }
        }
           stage('push to nexus') {
            steps {
                sh ''' echo "This is the push to Nexus Stage"
                 nexusArtifactUploader credentialsId: 'NEXUS_SYSTEM', 
                 groupId: 'teegroup', 
                 nexusUrl: 'jenkinserver.mycompany.com:8081', 
                 nexusVersion: 'nexus3', 
                 protocol: 'http', 
                 repository: 'timmyfirstnexus', 
                 version: 'OSS 3.34.0-01'
                '''
                
                
            }
        } 
        stage('Production') {
            steps {
                echo 'This is the Production release Confirmation Stage'
            }
        }
    }
}
