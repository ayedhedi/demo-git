pipeline {
    agent { docker { image 'maven:3.3.3' } }
    parameters {
            string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
     }
    stages {
        stage('build') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Example') {
            steps {
                echo "Hello ${params.PERSON}"
            }
        }
    }
}