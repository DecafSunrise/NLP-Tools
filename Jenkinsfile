pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Jenkins Test'
      }
    }

    stage('') {
      steps {
        mail(subject: 'Jenkins NLP-Tools Test', body: 'Something something Jenkins', from: 'Jenkins@IneedADomain.com')
      }
    }

  }
}