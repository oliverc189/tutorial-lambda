
node{
    stage('CheckOut') {
        git clone $(env.GIT_UTL)
    }

    stage('Build') {
        sh gradlew compileJava
    }
}