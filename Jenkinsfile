// Scripted//
node {
    stage('git'){
        git credentialsId: 'Github_ID', url: ' https://github.com/reachravi55/maven_demo.git'
    }
        stage ('maven validate'){
        sh 'mvn clean validate'
    }
    stage ('maven compile'){
        sh 'mvn clean compile'
    }
    stage ('maven test'){
        sh 'mvn clean test'
    }
    stage ('maven package'){
        sh 'mvn clean package'
    }
    stage ('maven verify'){
        sh 'mvn clean verify'
    }
    stage ('maven install'){
        sh 'mvn clean install'
    }
    stage ('deploy'){
        deploy adapters: [tomcat8(credentialsId: 'tomcat', path: '', url: 'http://54.81.242.27:8080/')], contextPath: null, onFailure: false, war: '**/*.war'
        
    }
}
