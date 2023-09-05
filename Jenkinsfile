
pipeline {
	agent {
			label "built-in"
	}
	
	stages {
				stage ("install-git") {
					steps {
					
							sh "yum install git -y"
					}
				}
				
				stage ("install-httpd-slave-1") {
				
				agent {
					
					label {
								label "built-in"
								customWorkspace "/mnt/velocity"
					}
				
				}
				
				steps {
							sh "sudo yum install httpd -y"
				}
					
				
				}
				
				stage ("install-httpd-git-slave-2") {
				
				agent {
					
					label {
								label "built-in"
								customWorkspace "/mnt/data"
					}
				
				}
				
				steps {
							sh "sudo yum install httpd git -y"
				}
					
				
				}
	}
}
