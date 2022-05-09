pipeline {
	agent {label 'slave2' }
		stages {
		
				stage('BUILD1') {
								
								agent {label 'slave1'}
								steps{
									sh ''' echo "this is build stage "
											sleep 5
											'''
											
								
								}
								}
		
				
				stage('DEPLOY1') {
				
									agent { label 'slave3' }
										steps{
										
										sh ''' echo "this is deploy stage "
												sleep 5
												'''
												
											}
									}
									
									
				stage('TEST1') {
				
								agent { label 'slave3'}
									steps{
											sh ''' echo "this is test stage"
											sleep 5
											'''
											
											}
								}
				
				
				}
				

		}
