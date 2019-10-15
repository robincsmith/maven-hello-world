node {
    stage('Setup') {
        sh 'rm -rf maven-hello-world'
        git 'https://github.com/robincsmith/maven-hello-world.git'
    }

    stage('Build') {
        sh 'mvn --batch-mode clean install -f my-app/pom.xml'
    }

    stage('Execute') {
        sh 'java -jar my-app/target/my-app-*.jar'
    }
}
