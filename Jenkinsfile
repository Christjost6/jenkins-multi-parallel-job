pipeline{
  agent any
  stages{
  	stage('version-control'){
  		steps{
  			git checkout
  		}
  	}
  	stage('parallel-job'){
  	  parallel{
  	  	stage('disk-free'){
  	  	  steps{
  	  	  	echo 'this to check disk free space'
  	  	  	sh 'df -h'
  	  	  }
  	  	}
  	  	stage('jenkins stat'){
  	  	  steps{
  	  	  	echo 'this is to check the current status of jenkins'
  	  	  	sh 'sudo symstemctl status jenkins'
  	  	  }
  	  	}
  	  }
  	}
  	stage('codebuild'){
  		steps{
  			sh 'cat /etc/passwd'
  		}
  	}
  }
}