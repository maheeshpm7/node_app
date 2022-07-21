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
sudo docker build /home/ubuntu/workspace/kaka/web1 -t nodeapp
sudo docker run -dit --name nodeap -p 8081:3000 nodeapp
sudo docker stop nodeap
'''
      }
    }

  }
}
