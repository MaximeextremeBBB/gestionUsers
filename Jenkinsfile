node {

stage('SCM'){
 git 'https://github.com/MaximeextremeBBB/gestionUsers'
}

stage('Compile'){
def mvnHome = tool name: 'maven-3' , type: 'maven'
sh "${mvnHome}/bin/mvn package"
}

stage('SonarQube') {
  def mvnHome = tool name: 'maven-3' , type: 'maven'
  sh "${mvnHome}/bin/mvn sonar:sonar -Dsonar.host.url=http://192.168.43.63:9000 -Dsonar.login=admin -Dsonar.password=ayari"
    }
}
