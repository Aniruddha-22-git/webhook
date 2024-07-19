pipeline{
  agent{
      label 'built-in'
    customWorkspace '/mnt/slave1'
  }
  stages{
    stage('stage1'){
      steps{
        sh "yum install httpd -y "
        sh "cp -r /mnt/slave1/index.html /var/www/html"
        sh "chmod -R 777 /var/www/html/index.html"
        sh "service httpd start"

      }
    }
  }
}
