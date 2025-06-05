pipeline{
  agent any
    tools{
      maven "Maven"
      jdk "JDK"
    }
    stages{
      stage('Checkout'){
        steps{
        git "https://github.com/Gekkorizz/Maven2"
        }
      }
      stage('build'){
        steps{
        sh "mvn clean install"
        }
      }
      stage('run'){
        steps{
        sh "exec:java -Dexec.mainClass="com.example.App"
        }
      }
    }
}
