library identifier: 'dockerBuilder@PROD', retriever: modernSCM(
  [$class: 'GitSCMSource',
   remote: "https://git.ellucian.com/scm/devops/jenkins-pipeline-docker.git"
  ]
)
node('ec2-worker-u18-medium') {
    stage('bootstrap') {
        cleanWs()
        dockerBuilder([restrictReleasesToMaster: false, publish: true, runUnitTests: false])
    }
}
