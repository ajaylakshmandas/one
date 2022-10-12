pipeline {
    agent any
    stages {
        stage('Example') {
            steps {
                echo 'Hello World'

                script {
                    bat '''git init
                    git branch
                    git status'''                    
                    def browsers = ['https://github.com/ajaylakshmandas/one.git', 'https://github.com/ajaylakshmandas/two.git','https://github.com/ajaylakshmandas/three.git']
                    for (int i = 0; i < browsers.size(); i++) {
                        echo "Testing the ${browsers[i]} browser"
                        bat """
                        git clone ${browsers[i]}
                        git branch
                        """ 
                    }
                }
            }
        }
    }
}
