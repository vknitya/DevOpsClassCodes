pipeline {
    agent any

    stages {
        stage('Compile') {
            steps {
                echo 'compiling..'
                sh 'mvn compile'
            }
        }
        stage('codereveiw') {
            steps {
                echo 'reveiw..'
                sh 'mvn pmd:pmd'
            }
        }
        stage('test') {
            steps {
                echo 'testing....'
                sh 'mvn test'
            }
        }
        stage('Metricheck') {
            steps {
                echo 'testing....'
                sh 'mvn cobertura:cobertura'
            }
        }
        stage('build') {
            steps {
                echo 'testing....'
                sh 'mvn package'
            }
        }
    }
}
