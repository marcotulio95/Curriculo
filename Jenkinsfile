pipeline {
  agent any
  stages {
    stage('Teste1') {
      parallel {
        stage('Teste1-A') {
          steps {
            addHtmlBadge(html: '<h1> OI </h1>', id: '123')
            echo 'OI'
          }
        }

        stage('Teste1-B') {
          steps {
            echo 'OI'
          }
        }

      }
    }

    stage('Teste2') {
      parallel {
        stage('Teste2-a') {
          steps {
            input(message: 'Testes OK', ok: 'testes OK ?', id: 'testing')
          }
        }

        stage('Teste-2b') {
          steps {
            echo 'teste 2b'
          }
        }

      }
    }

    stage('Teste3') {
      steps {
        input 'teste-3'
      }
    }

  }
}