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
        stage('Debug') {
            steps {
                echo "Ref: ${params.ref}"
            }
        }
        
        stage('Build') {
            when {
                expression {
                    params.ref == 'refs/heads/main'
                }
            }
            steps {
                echo 'Building...'
                // Add your build steps here
            }
        }
    }
}
