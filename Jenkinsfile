pipeline{
  agent {
    label 'built-in'
  }
  stages{
    stage('stage1'){
      steps{
        sh "yum install httpd -y "
        sh "service httpd start"
        sh "cp -r /mnt/webhook/index.html /var/www/html"
        sh "chmod -R 777 /var/www/html/index.html"
      }
    }
  }
}
