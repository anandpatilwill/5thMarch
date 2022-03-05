pipeline
{
	agent none
	stages 
	{
	stage ('Both build and Test')
	{
		parallel  
		{
			stage('Build')
                	{
                        	steps
				{
          				sh 'sleep 15; echo "This is Buid stage"'
				}
                	}
			stage('Test')
			{
				steps 
				{
				sh '''
				sleep 15
				echo "This is Test stage"
				'''
				}
			}
		}	
	}	
		stage('Deploy')
                {
		agent { label 'node2'}
                        steps
			{
				sh '''
				sleep 15
				echo "This is Deploy stage"
				'''
			}
                }
		stage('My stage')
                {
			agent { label 'node1'}
                        steps
			{
			sh '''
			sleep 15
			echo "This is my stage"	
			'''
			}
                }

	}
}
