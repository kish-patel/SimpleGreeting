node {
    stage('Checkout') {
        git url: 'https://github.com/kish-patel/SimpleGreeting.git'
    }
    
    stage('Gradle build') {
        bat 'gradle build -x test'
    }
    
    stage('User Acceptance Test') {
    	def response= input message: 'Is this build good to go?',
    	 parameters: [choice(choices: 'Yes\nNo',
    	 description: '', name: 'Pass')]
    	
    	if(response=="Yes") {
    	  stage('Deploy') {
    	   bat 'gradle build -x test'
    	  }
	    }
	}
}