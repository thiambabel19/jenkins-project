pipeline {
   agent any
   stages {
     stage(‘Build’) {
     steps {
       sh "/opt/java/openjdk/bin/mvn clean package"
     }
   }
   stage(‘Test’) {
     steps {
         sh "/opt/java/openjdk/bin/mvn test"
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