pipeline {
    agent any

    stages {
        stage('Sonar Analysis') {
            steps {
                echo 'LMS code Analysis'
                sh 'cd webapp && sudo docker run --rm -e SONAR_HOST_URL=http://18.201.161.83:9000/ \
                  -e SONAR_TOKEN=sqp_3c43410eed28e1b33d5090babaac14ef9863060e \
                  -v "$(pwd):/usr/src" sonarsource/sonar-scanner-cli \
                  -Dsonar.projectKey=LMS -X'
            }
        }


    }
}
