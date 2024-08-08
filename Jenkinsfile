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
    stage("Build gradlew build){
          sh '''
            gradlew build --no-daemon
          '''
    }
    stage("Archive a build"){
        archiveArtifacts artifacts: 'dist/trainSchedule.zip', fingerprint: true, followSymlinks: false
    }
  }

}
