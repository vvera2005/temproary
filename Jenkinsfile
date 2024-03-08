pipeline {
    agent any
    
    triggers {
        GenericTrigger(
            genericVariables: [
                [key: 'ref', value: '$.ref']
            ],
            causeString: 'GitHub Push Event'
        )
    }
    
    stages {
        stage('Build') {
            when {
                expression {
                    params.ref == 'refs/remotes/origin/main'
                }
            }
            steps {
                echo 'Building...'
                // Add your build steps here
            }
        }
    }
}
