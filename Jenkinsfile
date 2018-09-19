pipeline
{
  agent any
  stages {
   stage('Checkout and build')
   {
     steps
     {
      sh 'echo "checkout of source code..."'
      sh 'ansible-playbook /home/kpit/Desktop/playbooks/test-playbooks/scm.yaml'
      }
      post {
         success {
            sh 'echo "compiling the code and downloding the war file..."'
            sh 'cd /home/kpit/Desktop/playbooks/checkouts/course-api'
            sh 'mvn clean install'
                }
            }
    }
    
    }
    }

