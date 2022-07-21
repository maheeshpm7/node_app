pipeline {
  agent {
     node { 
        label 'bty'
        } 
  }
  stages {
    stage('Checkout Scm') {
      steps {
        git 'https://github.com/maheeshpm7/node_app.git'
      }
    }

    stage('Shell script 0') {
      steps {
        sh '''sudo docker rm -f nodeap
sudo docker build /home/ubuntu/workspace/pipe-jenki -t nodeapp
sudo docker run -dit --name nodeapps -p 8082:3000 nodeapp
sudo docker stop nodeapps
'''
      }
    }

  }
}
