pipeline{
	agent any
	stages{
		stage("Stage 1: build java project"){
			steps{
				build 'Java Project'
			}
		}
		stage("Stage2: echo"){
			steps{
				echo "Hello Gursimran"
			}
		}
		stage("Stage3: if-else"){
			steps{
				if (env.BRANCH_NAME == 'master'){
					echo "Master branch"
				}
				else{
					echo "Not master branch"
				}
			}
		}
	}
}