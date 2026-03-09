// pipeline {
//     agent any

//     stages {
//         stage('Fetch') {
//             steps {
//                 echo 'Fetching from repo'
//                 git 'https://github.com/aslin-123/DevopsPractical.git'
//             }
//         }
//         stage('Build') {
//             steps {
//                 echo 'Building in progress'
//                 bat 'javac hello.java'
//             }
//         }
//         stage('Execute') {
//             steps {
//                 echo 'Executing...'
//                 bat 'java hello.java'
//             }
//         }
//            post{
//         success{
//             echo 'Pipeline build Successfuly'
//         }
//         failure{
//             echo 'Pipeline Failed'
//         }
//     }
//     }
// }
pipeline{
   agent any

   stages{
      stage('Checkout'){
          steps{
              git 'https://github.com/aslin-123/DevopsPractical.git'
          }

      }
      stage('Publish'){
            steps{
                publishHTML([
                   allowmissing:true,
                   alwaysLinktoLastBuild:false,
                   KeepAll:false,
                   reportDir:'.',
                   reportFiles:'Index.html',
                   reportName:'MY HTML PAGE'
                ])
            }
      }
   }

}
