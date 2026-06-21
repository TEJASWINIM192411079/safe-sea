pipeline {

```
agent any

stages {

    stage('Checkout') {
        steps {
            checkout scm
        }
    }

    stage('Stop Old Containers') {
        steps {
            sh 'docker-compose down'
        }
    }

    stage('Build Images') {
        steps {
            sh 'docker-compose build'
        }
    }

    stage('Start Containers') {
        steps {
            sh 'docker-compose up -d'
        }
    }

    stage('Show Running Containers') {
        steps {
            sh 'docker ps'
        }
    }

    stage('Show Logs') {
        steps {
            sh 'docker-compose logs'
        }
    }
}
```

}
