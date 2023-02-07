pipeline {
    agent {
        label {
            label 'mater_node01'
        }
    }
    stages{
        stage('Fetch'){
            steps{
              sh '''
                    rm -rf k8s 
                    git clone https://github.com/jonny-levi/k8s.git
                '''
            }
        }
        
        stage('Build'){
            steps{
                sh ''' 
                       python3 k8s/scripts/pig_game.py
                        '''
            }
        }
        
    }
}