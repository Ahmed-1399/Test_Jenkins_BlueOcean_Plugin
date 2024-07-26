pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build Completed...'
      }
    }

    stage('Test Stages') {
      parallel {
        stage('Test1') {
          steps {
            echo 'Running Test1'
          }
        }

        stage('Test2') {
          steps {
            echo 'Running Test2'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        input(message: 'Are you sure to Deploy?', ok: 'Yes, Iam sure')
        echo 'Deploy Completed...'
      }
    }

    stage('Notift for new build') {
      steps {
        echo 'Notify build completed successfully'
      }
    }

  }
}