node {
    stage('SCM Checkout'){
       git 'https://github.com/mofrobby/simple-java-maven-app'
    }
    stage('Compile-Package'){
        sh 'mvn package'
    }
}
