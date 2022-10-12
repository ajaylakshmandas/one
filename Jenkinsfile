pipeline {
    agent any
    stages {
        stage('Example') {
            steps {
                echo 'Hello World'

                script {
                    bat '''git init '''
                    def repo = ['checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: '59d28281-60c8-4274-87c4-4369bc590b38', url: 'https://github.com/ajaylakshmandas/one.git']]])']
                    for (int i = 0; i < repo.size(); ++i) {
                        echo "Testing the ${repo[i]} browser"
                        bat """
                        git remote set-url origin ${repo[i]}
                        git init
                        git checkout test
                        git pull origin test
                        git checkout dev
                        git pull origin dev
                        git merge test
                        git push origin dev



                        
                        """ 
                    }
                }
            }
        }
    }
}
