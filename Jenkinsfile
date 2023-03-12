pipeline {
    agent { label 'docker' }
    stages {
        stage('vcs') {
            steps {
                git branch: 'rel_1_sprint',
                    url: 'https://github.com/satya36-cpu/StudentCoursesRestAPI.git'
            }
        }
        stage('build') {
            steps {
                sh 'docker image build -t satyabrata36/spc2:latest .'
            }
        }
        stage('scan'){
            steps {
                sh 'echo docker scan satyabrata36/spc2:latest '
                sh 'docker image push satyabrata36/spc2:latest'
            }
        }
    }
}        