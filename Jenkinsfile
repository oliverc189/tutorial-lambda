pipeline{
stages{
    stage('CheckOut') {
        checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'GitHub', url: 'https://github.com/oliverc189/tutorial-lambda.git']]])
    }

    stage('Build') {
        sh gradlew compileJava
    }
    }
}