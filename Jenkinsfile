pipeline {
	agent {label 'master' }
							parameters {
			  string defaultValue: 'test', description: 'which env should be build need to deploy', name: 'TEST'
			}

		stages {
		
				stage('BUILD1') {
								
								agent {label 'slave1'}
								steps{
									catchError(buildResult : 'SUCCESS' , stageResult : 'FAILURE'){
									sh ''' exit 0
									
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
