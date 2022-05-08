pipeline 
{
		agent none {
				stages {
			
						stage(BUILD1){
								agent { label (slave1)}
								steps {
								
									sh ''' echo "this build"
									sleep 5
									'''
									}
						}
						
						
						stage(DEPLOY1){
								agent { label (slave2)}
								steps {
								
									sh ''' echo "this DEPLOY "
									sleep 5
									'''
										}
									}
						
						
						stage(TEST1){
								agent { label (slave3)}
									steps {
										sh ''' echo "this TEST"
											sleep 5
											'''
											}
											
						}
						
						
				}
