pipeline {
  agent {
    docker {
      image "arm64v8/maven:3-eclipse-temurin-21-alpine" /* (1) */
      args -v "/tmp/.m2:/tmp/.m2" /* (2) */
    }
  }

  stages {
    stage("Build") {
      steps {
        sh "mvn -B -DskipTests -Dmaven.repo.local=/tmp/.m2/repository clean package" /* (3) */
      }
    }
  }
}
