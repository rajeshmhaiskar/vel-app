pipeline {

	agent {
		label "built-in" 
	}
	stages {
		stage ("install-git") {
		agent {
		label {
		label "slave-1"
		customWorkspace "/mnt/pipeline"
		steps {
		sh "yum install git -y"
		}
		
		}}}
 		stage ("install-httpd")
		agent {
		label {
		label "slave-2"
		customWorkspace "/mnt/data"
		steps {
		sh "yum install httpd -y"
		}

		}}}
		/*stage ("install-httpd-git")
		agent any
		customWorkspace "/mnt/uat"
		steps {
		sh "yum install git -y"
		}
		}}}*/
}}
