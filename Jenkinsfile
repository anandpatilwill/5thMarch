pipeline
{
	agent any
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
          				sh 'sleep 15;echo "This is Buid stage"'

				}
                	}
			stage(Test)
			{
				steps 
				{
				sh '''
				sleep 15
				echo "This is Test stage"
				}
			}
		}	
	}	
		stage(Deploy)
                {
                        steps
			{
			sh '''
			echo "This is Deploy stage"
			sleep 15

                }
		stage(My stage)
                {
                        steps
			{
			sh '''
			echo "This is my stage"	
			}
                }



	}



}
