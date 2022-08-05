pipeline {
    agent {
        docker { image 'doctoolchain/doctoolchain-jenkins-ssh-agent:v2.0.5' }
    }

    stages {
        stage('Generate Docs and check link sanity') {
            steps {
                sh "doctoolchain . -PmainConfigFile=docToolchainConfig.groovy generateHTML htmlSanityCheck"
            }
        }
    }
}