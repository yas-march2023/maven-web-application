node{

def mavenHome =  tool name: "maven3.9.4"

stage('checkoutcode'){
git branch: 'development', credentialsId: '90b1fd7c-ca36-4c7d-9c87-c9f80a3b13a8', url: 'https://github.com/yas-march2023/maven-web-application.git'
}

stage('Build'){
    sh "${mavenHome}/bin/mvn clean package"
}
/*
stage('ExecuteSonarQubeReport'){
    sh "${mavenHome}/bin/mvn clean sonar:sonar"
}
stage('uploadArtifcatsIntoNexus'){
    sh "${mavenHome}/bin/mvn clean deploy"

}
stage('DeployAppIntoTomcatServer'){
    sshagent(['ec2-user']) {
        sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@172.31.8.16:/opt/apache-tomcat-9.0.80/webapps"

}
}
*/
}//node closing
