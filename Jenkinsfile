@Library('printuser')_
									getUser 'MONICA', 'TRAINEE'
pipeline {
	agent {label 'master' }
							
		stages {
		
				stage('BUILD1') {
								
								agent {label 'slave1'}
								steps{
									catchError(buildResult: 'SUCCESS', stageResult: 'FAILURE'){
									sh ''' 

									
											'''
									}		
								
								}
								}
				stage('TEST and DEPLOY') {
									input {
					  message 'press yes to continue'
					}

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
