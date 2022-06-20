pipeline {
    
    agent {
        dockerfile {
            dir 'image'
        }
    }
    
    stages {
        stage ('Lanzar playbook') {
            steps {
                sh 'ansible-playbook -i /data/inventarios/aws /data/playbooks/nginx/playbook.yaml'
            }
        }
    }
    
}