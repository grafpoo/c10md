stage("Build Info") {
  node {
    def tag = "${env.BRANCH_NAME}.${env.BUILD_NUMBER}"
    def service = "c10md:${tag}"
    def commit = checkout scm
    echo "latest commit id: ${commit.GIT_COMMIT}"
    stage('Build') {
      docker.build("${service}")
    }
  }
}
