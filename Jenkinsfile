pipeline {
    agent any
    stages {
        stage('Example') {
            steps {
                echo 'Hello World'

                script {
                    bat '''git init '''
                    def browsers = ['https://github.com/ajaylakshmandas/one.git', 'https://github.com/ajaylakshmandas/two.git']
                    for (int i = 0; i < browsers.size(); ++i) {
                        echo "Testing the ${browsers[i]} browser"
                        bat """
                        git clone ${browsers[i]}
                        git checkout dev
                        git pull origin dev
                        """ 
                    }
                }
            }
        }
    }
}
