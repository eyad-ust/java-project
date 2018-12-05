node('linux') {   
	stage('Unit Tests') {
    		sh 'ant'
		sh 'ant -f test.xml -v' 
		junit 'reports/result.xml'
	}
	stage('Build') {
		sh 'ant'
		sh 'ant -f build.xml -v' 
	}
	stage('Deploy') {
		sh 'sudo aws s3 cp https://github.com/eyad-ust/java-project/blob/master/lib/junit-4.10.jar s3://eyad-eyad-demo'	
	}
}
