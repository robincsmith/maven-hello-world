node {
    stage('Setup') {
        sh 'rm -rf *'
        checkout scm
    }

    stage('Build') {
        sh 'mvn --batch-mode clean install -f my-app/pom.xml'
    }

    stage('Execute') {
        sh 'java -jar my-app/target/my-app-*.jar'
    }
}
