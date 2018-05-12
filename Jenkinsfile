pipeline{
    stage('CheckOut') {
        checkout scm
    }

    stage('Build') {
        sh gradlew compileJava
    }
}