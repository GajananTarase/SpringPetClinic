pipeline{
    agent{label 'master'}
    tools{maven 'M3'}
    stages('Chckout'){
        steps{
            gt branch: 'main', url:'https://github.com/GajananTarase/SpringPetClinic.git'
        }
    }
    stage('Build'){
        steps{
            sh 'mvn compile'
        }
    }
    stage('Test'){
        steps{
            sh 'mvn test'
        }
    }
    stage('Package')
    {
        steps{
            sh 'mvn package'
        }
    }
    stage('Deploy'){
        steps{
            sh 'java -jar / var/lib/jenkins/workspace/PetclinicDeclrative/target*.jar'
        }
    }
}
