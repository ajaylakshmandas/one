pipeline {
    agent any
    stages {
        stage('Example') {
            steps {
                echo 'Hello World'
<<<<<<< HEAD

                script {
                    bat '''git init '''
                    def repo = ['https://github.com/ajaylakshmandas/one.git','https://github.com/ajaylakshmandas/two.git']
                    for (int i = 0; i < repo.size(); ++i) {
                        echo "Repo ${repo[i]} "
                        bat """
                        git remote set-url origin ${repo[i]}
                        git init
                        git fetch --all
                        git checkout test
                        git pull origin test --allow-unrelated-histories  
                        git checkout dev
                        git pull origin dev --allow-unrelated-histories 
                        git merge upstream/test
                        git push origin dev                        
                        """ 
                    }
                }
=======
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: '59d28281-60c8-4274-87c4-4369bc590b38', url: 'https://github.com/ajaylakshmandas/one.git'], [credentialsId: '59d28281-60c8-4274-87c4-4369bc590b38', url: 'https://github.com/ajaylakshmandas/two.git'], [credentialsId: '59d28281-60c8-4274-87c4-4369bc590b38', url: 'https://github.com/ajaylakshmandas/three.git']]])      
>>>>>>> d870f992081795f79f5b25627a7714c433aca749
            }
        }
    }
}
