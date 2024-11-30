pipeline{
  agent any 
  stages{
    stage('clone'){
      steps{
        git 'https://github.com/devarsh82/demo-react.git'
      }
    }
    stage('install packages'){
      steps{
        sh 'npm install'
      }
    }
    stage('build the application'){
      steps{
        sh 'npm run build'
      }
    }    
    stage('delete old application'){
      steps{
        sh 'rm -rf /var/www/html/*'
      }
    }
    stage('deploy the application'){
      steps{
        sh 'cd build && cp -r * /var/www/html/'
      }
    }
  }
}
