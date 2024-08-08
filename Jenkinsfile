pipeline{
  agent any
  stages {
    stage("Git clone"){
        checkout scmGit(
          branches: [[name: "*/master"]],
          userRemoteConfigs:[[
            url:"https://github.com/gbigbi/cicd-pipeline-train-schedule-pipelines.git"
          ]]
        )
    }
  }

}
