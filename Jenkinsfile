pipeline {
    agent any
    stages {
        stage('Example') {
            steps {
                echo 'Hello World'

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
                        git pull --rebase development
                        git pull origin test --allow-unrelated-historiesorigin 
                        git checkout dev
                        git pull origin dev --allow-unrelated-historiesorigin
                        git merge upstream/test
                        git push origin dev                        
                        """ 
                    }
                }
            }
        }
    }
}
