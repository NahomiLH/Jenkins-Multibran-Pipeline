pipeline {
	agent any
	environment{
		EXECUTE = 'true'
}
		stages {
			stage('First') {
				steps {
					sh 'echo "Step One"'
				}
			}
			stage('Second') {
				when {
					environment name: 'EXECUTE', value: 'true'
}
				steps {
					sh 'echo "Step Two"'
					sh 'echo "Updating Second Stage"
				}
			} 
			stage('Third') {
				when {
					environment name: 'EXECUTE', value: 'false'
}
				steps {
					sh 'echo "Step Three"'
				}
			}
		}
}
