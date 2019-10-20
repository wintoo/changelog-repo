node {
    stage('checkout branch '+ "${BRANCH_NAME}" ){
        println ("Branch Name =" + "${BRANCH_NAME}")
    }
    
    stage('Build'){
        echo 'first stage'
    }
    
    if("${BRANCH_NAME}" == 'dev') {
        stage ('sonarqube code analysis') {
            echo 'sq scanning'
        }
        
        stage ('upload to dev') {
            echo 'uploading to dev'
        }
    else if ("${BRANCH_NAME}" == 'master') {
        stage ('deploy to qa') {
            echo 'deploy to dev'
        }    
    }
}
