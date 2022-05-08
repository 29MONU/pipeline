pipeline {
	agent any 
		stages {
			stage('Build') {
				steps {
					sh '''echo STAGE1: This is a build stage
							sleep 5 '''
					}
					}
					stage('Test') {
						steps{
							sh '''echo STAGE2: This is test stage
									sleep 5 '''
							}
					}
					stage('Deploy') {
							steps{
								sh '''echo STAGE3: This is deploy stage
										sleep 5 '''
								}
							}
						}
					}
