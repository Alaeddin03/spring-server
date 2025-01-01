pipeline {
    agent any
    stages {
        stage("BlackDuckSecruityScan") {
            steps {
                script {
                    def status = security_scan product: "coverity", coverity_stream_name: "jenkins-test", coverity_project_name: "jenkins-test"
                        // mark_build_status: 'UNSTABLE'
                    
                    // Uncomment to add custom logic based on return status
                    // if (status == 8) { unstable 'policy violation' }
                    // else if (status != 0) { error 'plugin failure' }
                }
            }
        }
    }
}
