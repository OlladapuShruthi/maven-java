// node{
//   stage('Build'){
//         echo 'started building...'
//         bat 'mvn clean insatll'

//     }
//   stage('Test'){
//     echo 'started testing...'
//     bat 'mvn test'
//   }
//   stage('Deploy'){
//     echo 'started Deploying...'
//     bat 'mvn deploy'
//   }
  
// }
node {
    properties([
        pipelineTriggers([
            [$class: 'GitHubPushTrigger']
        ])
    ])

    stage('Build') {
        bat 'mvn clean install'
    }

    stage('Test') {
        bat 'mvn test'
    }

    stage('Deploy') {
        bat 'echo Deployment Completed'
    }
}
