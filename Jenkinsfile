pipeline {
    agent any
    stages {
        stage('Compile Code') {
            steps {
                sh '/opt/maven/bin/mvn compile'
            }
        }
        stage('PMD Code Review') {
            steps {
                sh '/opt/maven/bin/mvn -P metrics pmd:pmd'
            }
            post {
                success {
                    recordIssues(tools: [pmdParser(pattern: '**/pmd.xml')])
    stage('Compile Code') {
    steps {
        echo 'Running mvn compile...'
        sh '/opt/maven/bin/mvn compile'
                }
            }
        }
        stage('Package Application') {
            steps {
                sh '/opt/maven/bin/mvn package'
    stage('Compile Code') {
    steps {
        echo 'Running mvn compile...'
        sh '/opt/maven/bin/mvn compile'
            }
        }
    }
}
