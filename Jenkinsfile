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
		parallel{
			stage("Stage3: if branch is master"){
				when{
						branch "master"
				}
				steps{
						echo "Master branch"
				}
			}
			stage("Stage4: waiting for input"){
				steps{
						input("Continue or not?")
				}
			}
			stage("Stage5: if branch is not master"){
				when{
					not{
						branch "master"
					}
				}
				steps{
						echo "Not master branch"
				}
			}
		}
	}
}