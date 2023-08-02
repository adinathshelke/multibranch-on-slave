pipeline {
  agent {
    label {
      label "master"
      customWorkspace "/mnt/multibranch-slave"
    }
  }
  stages {
    stage ("clean workspace") {
      steps {
        cleanWs()
      }
      }
    stage ("deploy on master"){
      steps {
        sh "git clone https://github.com/adinathshelke/multibranch-on-slave.git"
      }
      
    }
  }
}
