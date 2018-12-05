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
}
