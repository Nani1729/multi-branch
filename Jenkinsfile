pipeline {
  agent any
  stages {
    stage('stage-1') {
      steps {
        echo 'this is stage ONE'
      }
    }
    stage('stage-2') {
      steps {
        echo 'this is stage TWO'
      }
    }
    stage('Test') {
            when {
                not { branch 'master' } // Execute only if the branch is 'master'
            }
            steps {
                echo 'this is master branch'
            }
        }
    stage('Test-6') {
            when {
                branch 'branch-4' // Execute only if the branch is 'master'
            }
            steps {
                echo 'this is branch-4'
            }
        }
    stage('stage-3') {
      steps {
        echo 'this is stage THREE'
      }
    }
    stage('stage-4') {
      steps {
        echo 'this is stage FOUR'
      }
    }
    stage('Get Branch Name') {
            steps {
                script {
                    def branchName = env.BRANCH_NAME
                    echo "Current branch is: ${branchName}"
                }
            }
        }
  }
}
        
