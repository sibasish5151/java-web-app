node {
    stage ('checkout code') {
        git branch:'main', url:'https://github.com/sibasish5151/java-web-app.git'
    }
    stage ('build code') {
        sh '/opt/maven/bin/mvn clean package'
    }
    stage ('deploy to tomcat') {
        deploy adapters:[tomcat9(url:'http://65.2.151.89:8080', credentialsId:'tomcatcred')], war:'**/*.war'
    }
}