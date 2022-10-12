pipeline {
    agent any
    stages {
        stage('Example') {
            steps {
                echo 'Hello World'

                script {
                    bat '''git init '''
                    def repo = ['https://github.com/ajaylakshmandas/one.git', 'https://github.com/ajaylakshmandas/two.git']
                    for (int i = 0; i < repo.size(); ++i) {
                        echo "Testing the ${repo[i]} browser"
                        bat """
                        git branch
                        git status
                        git remote set-url origin ${repo[i]}
                        git clone ${repo[i]}
                        git status
                        git branch
                        git checkout dev
                        git pull origin dev
                        """ 
                    }
                }
            }
        }
    }
}
