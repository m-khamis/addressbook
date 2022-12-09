pipeline {
    agent any

    stages {
        stage ("clone"){
            steps {
            git "https://github.com/m-khamis/addressbook"
            }
        }
        stage ("compile") {
            steps {
                echo "executing compilation"
                sh "mvn compile"
            }
        }
        stage ("tests"){
            steps {
                echo "executing tests"
                sh "mvn test"
            }
        }
        stage ("package") {
            steps {
                echo "creating a package"
                sh "mvn package"
            }
        }
    }
}
