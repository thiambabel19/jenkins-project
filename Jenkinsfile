pipeline {
   agent any
   stages {
     stage(‘Build’) {
     steps {
       sh "/var/jenkins_home/tools/hudson.tasks.Maven_MavenInstallation/Maven/bin/mvn clean package"
     }
   }
   stage(‘Test’) {
     steps {
         sh "/var/jenkins_home/tools/hudson.tasks.Maven_MavenInstallation/Maven/bin/mvn test"
       }
     }
   }
}


// pipeline {
//   agent any
//   tools{
//       maven 'maven'
//   }
//   stages {
//     stage('Build') {
//       steps {
//         sh "mvn clean package -DskipTests"
//       }
//     }
//     stage('Build Docker image') {
//       steps {
//         sh "docker build -t jenkinsproject:v1 ."
//       }
//     }
//     stage('Deploy') {
//       steps {
//         sh "docker run --name jenkinsproject -d -p 8080:8080 jenkinsproject:v1"
//       }
//     }
//   }
// }