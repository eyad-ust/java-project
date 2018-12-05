node('linux') {   
	stage('Unit Tests') {
    'ant'
		sh 'ant -f test.xml -v' 
		junit 'reports/result.xml'
	}
	stage('Build') {
      'ant'
	    sh 'ant -f build.xml -v' 
	}
	stage('Deploy') {
	'sudo aws s3 cp https://github.com/eyad-ust/java-project/blob/master/lib/junit-4.10.jar s3://eyad-eyad-demo'	
	}
}
