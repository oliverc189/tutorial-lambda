node {
    // Clean workspace before doing anything
    deleteDir()

    try {
        stage ('Clone') {
             checkout scm
        }
        stage ('Build') {
             sh ./gradlew bootJar
        }
        stage ('Tests') {
            parallel 'static': {
                sh "echo 'shell scripts to run static tests...'"
            },
            'unit': {
                sh ./gradlew test
            }
        }
        stage ('Deploy') {
            sh "echo 'shell scripts to deploy to server...'"
        }
    } catch (err) {
        currentBuild.result = 'FAILED'
        throw err
    }
}




