
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
								label "slave-1"
								customWorkspace "/mnt/pipeline"
					}
				
				}
				
				steps {
							sh "sudo yum install httpd -y"
				}
					
				
				}
				
				stage ("install-httpd-git-slave-2") {
				
				agent {
					
					label {
								label "slave-2"
								customWorkspace "/mnt/pipeline"
					}
				
				}
				
				steps {
							sh "sudo yum install httpd git -y"
				}
					
				
				}
	}
}
