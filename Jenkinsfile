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
                        git pull origin test  
                        git checkout dev
                        git pull origin dev 
                        git merge test
                        git push 
                        """ 
                    }
              }
        }
    }
}
