pipeline{
    agent{
        label 'AGENT-1'
    }

    options{
        timeout(time: 45, unit: 'MINUTES')
        disableConcurrentBuilds()
        ansiColor('xterm')
    }

    parameters{
        string(name: 'appVersion', defaultValue: '1.0.0', description: 'Which Version to Deploy?')
    }

    environment{
        def appVersion = ""
        def nexusUrl = "nexus.harshadevops.site:8081"
    }

    stages{
        stage('Print the Application Version'){
            steps{
                sh """
                    echo "Application Version: ${params.appVersion}"
                """
            }
        }
    }
}