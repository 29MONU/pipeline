pipeline {
	agent none 
		stages {
			stage('Build') {
			
				agent { label 'slave1'}
				
					steps {
						sh '''echo STAGE1: This is a build stage
							sleep 5 '''
					}
					}
					stage('Test') {
					
					agent { label 'slave2'}
					
						steps{
							sh '''echo STAGE2: This is test stage
									sleep 5 '''
							}
					}
					stage('Deploy') {
					
					agent { label 'slave3'}
					
					steps{
								sh '''echo STAGE3: This is deploy stage
										sleep 5 '''
								}
							}
						}
					}
				
