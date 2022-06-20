pipeline {
    
    agent {
        dockerfile {
            dir 'image'
        }
    }
    
    stages {
        stage ('Lanzar playbook') {
            steps {
                sh 'ansible-playbook -i /var/jenkins_home/workspace/Buena/ansible/inventarios/aws /var/jenkins_home/workspace/Buena/ansible/playbooks/nginx/playbook.yaml'
            }
        }
    }
    
}