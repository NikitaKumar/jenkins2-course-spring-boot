node {
    stage('checkout') {
        git 'https://github.com/NikitaKumar/jenkins2-course-spring-boot.git'
    }
    
    def project_path="spring-boot-samples/spring-boot-sample-atmosphere"
    
    dir(project_path) {        
        stage('compile, test, package') {
            bat 'mvn clean package'
        }
    
        stage('archival') {
            archiveArtifacts artifacts: "/target/*.jar", excludes: null  
        }
    }
}