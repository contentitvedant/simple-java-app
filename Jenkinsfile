pipeline{
	agent any 
	tools {
	maven "mvn"
}


	stages{
	stage('clone'){
	steps {
	git branch: 'main', url: 'https://github.com/contentitvedant/simple-java-app.git'
	}
	}

	stage('build'){
        	steps {
		sh 'mvn clean install'
        }

        }

	stage('artifact'){	
        	steps {
		archiveArtifacts artifacts: 'target/*.jar', followSymlinks: false
        }
        }






	}
}
