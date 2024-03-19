pipeline {
    tools {
        maven "Maven3"
    }
    agent any
    
        stages {
            stage ('Checkout from git'){
                steps {
                    git branch: 'main', url: 'https://github.com/bkrrajmali/springbootapp.git'
            }
        }
        stage ('Maven Build'){
                steps {
                   sh 'mvn clean install'
            } 
        }
        stage ('Unit Test'){
            steps {
                echo '<----------------------Unit Test Under Progess------------------>'
                sh 'mvn surefire-report:report'
                echo '<----------------------Unit Test Done------------------>'
            }
        }
    }
}
