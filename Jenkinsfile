pipeline{
stages{
    stage('CheckOut') {
        checkout scm
    }

    stage('Build') {
        sh gradlew compileJava
    }
    }
}