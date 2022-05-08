pipeline{

	agent none	
		stages {
			stage(BUILD1){
				agent { label (slave1)}
					stage {
							sh ''' echo "this is build "
									sleep 5 '''
							}
							}
							
							
			stage (DEPLOY1) {
				agent { label (slave2) }
					stage {
						sh ''' echo "This is deploy stage"
								sleep 5 '''
							}
							}
							
			stage (TEST1){
				agent {label (slave3)}
					stage {
							sh '''echo "this is test "
									sleep 5 '''
								}
								}
				}
		}
