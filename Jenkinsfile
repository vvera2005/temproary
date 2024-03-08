pipeline {
    agent any
    
    triggers {
        GenericTrigger(
            genericVariables: [
                [key: 'ref', value: '$1376abc6-dd36-11ee-8272-2c6ad7275de6.ref']
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
