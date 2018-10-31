pipeline {
	// Each stage must specify its own agent
	agent none
	stages {
		stage('Build') {
			agent {
				docker {
					image 'python:2-alpine'
				}
			}

			steps {
				sh 'python -m py_compile sources/add2vals.py sources/calc.py'
			}
		}
	}
}
