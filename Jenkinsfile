pipeline {
  agent {
    label {
      label "slave2"
      customWorkspace "/mnt/multibranch-slave"
    }
  }
  stages {
    stage ("clean workspace") {
      steps {
        cleanWs()
      }
      }
    stage ("deploy 23Q3 branch on slave2"){
      steps {
        sh "git clone https://github.com/adinathshelke/multibranch-on-slave.git -b 23Q3"
        sh "cp -r /mnt/multibranch-slave/multibranch-on-slave/index.html /var/www/html/"
        sh "chmod -R 777 /var/www/html/index.html"
      }
      
    }
  }
}
