pipeline {
  agent any
  
  stages {
    stage ("Test") {
      steps {
        echo "Testing"
      }
    }
    
    stage ("Deploy") {
      steps {
        echo "Deploying"
      }
    }
    
    stage ("Report") {
      steps {
        echo "Job done" > report.txt
      archiveArtifacts allowEmptyArchive: true, artifacts: 'report.txt', fingerprint: true, followSymlinks: false, onlyIfSuccessful: true
      }
    }
  }
}
