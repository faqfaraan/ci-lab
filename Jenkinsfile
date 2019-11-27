
 node {
   stage('checkout sources') {
         // You should change this to be the appropriate thing
         git url: 'https://github.com/faqfaraan/ci-lab'
   }
 try{
   stage('Build') {
     // you should build this repo with a maven build step here
     withMaven (maven: 'maven3') {
                    sh "mvn package"
                  }
   }
       } finally {
           junit 'target/surefire-reports/**/*.xml'
       }

 }

