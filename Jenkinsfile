node {
    git branch: 'main', url 'https://github.com/mahmoudghanem1/simple-java-app.git'
    stage('build'){
        try{
        sh 'echo" build stage "'    }
        catch(Execption e){
            sh'ehco"expetion found "'
            throw e
        }
    }
    stage('test'){
        if (env.BRANCH_NAME == "feat"){
            sh'echo"test stage"'
        }
        else{
            sh'echo "ship test stage "'
        }
    }
}