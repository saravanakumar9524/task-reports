pipeline {
    agent any

    stages {
        stage('Update browser') {
            steps {
                nodejs(nodeJSInstallationName: 'sample') {
                    bat 'npx browserslist@latest --update-db'
                }
            }
        }
        stage('Install') {
            steps {
                nodejs(nodeJSInstallationName: 'sample') {
                    bat 'npm install'
                }
            }
        }
        stage('Build') {
            steps {
                nodejs(nodeJSInstallationName: 'sample') {
                    bat 'npm run build'
                }
            }
        }
    }
}
