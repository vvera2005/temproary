pipeline {
  agent any
  triggers {
    GenericTrigger(
      genericVariables: [
        [key: 'ref', value: '$.ref']
      ]
    )
  }
  stages {
    stage('Some step') {
      steps {
        script {
          echo "${params.ref}"
        }
      }
    }
  }
}
