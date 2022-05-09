pipeline {
	agent {label 'slave2' }
				environment {
			  TEST = "test"
			}

		stages {
		
				stage('BUILD1') {
								
								agent {label 'slave1'}
								steps{
									sh ''' echo "this is build stage : $TEST "
											sleep 5
											'''
											
								
								}
								}
				stage('TEST and DEPLOY') {
					parallel{
				
				
												stage('DEPLOY1') {
												
																	agent { label 'slave3' }
																		steps{
																		
																		sh ''' echo "this is deploy stage : $TEST "
																				sleep 5
																				'''
																				
																			}
																	}
																	
																	
												stage('TEST1') {
												
																agent { label 'slave3'}
																	steps{
																			sh ''' echo "this is test stage : $TEST"
																			sleep 5
																			'''
																			
																			}
								
								}
					}
				}
				}
				

		}
