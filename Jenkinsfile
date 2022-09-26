pipeline {
  agent any
  
  stages {
    stage ("Test") {
      echo "Testing"
    }
    
    stage ("Deploy") {
      echo "Deploying"
    }
    
    stage ("Report") {
      echo "Job done" > report.txt
      archiveArtifacts allowEmptyArchive: true, artifacts: 'report.txt', fingerprint: true, followSymlinks: false, onlyIfSuccessful: true
    }
  }
}
