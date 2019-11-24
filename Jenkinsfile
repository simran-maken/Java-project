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
		stage("Stage3: parallel"){
			parallel{
				stage("Stage 3a: if branch is master"){
					when{
							branch "master"
					}
					steps{
							echo "Master branch"
					}
				}
				stage("Stage 3b: waiting for input"){
					steps{
							input("Continue or not?")
					}
				}
				stage("Stage 3c: if branch is not master"){
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
}