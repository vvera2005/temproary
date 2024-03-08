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
                    genericVariables.ref == 'refs/heads/main'
                }
            }
            steps {
                echo 'Building...'
                // Add your build steps here
            }
        }
    }
}
