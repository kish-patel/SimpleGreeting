node {
    stage('Checkout') {
        git url: 'https://github.com/kish-patel/SimpleGreeting.git'
    }
    
    stage('Gradle build') {
        bat 'gradle build'
    }
}