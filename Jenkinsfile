node{
    stage('SCM checkout'){
    git 'https://github.com/dvkrish5/panda/new/master'
    }
    stage('compile-Package'){
        sh "${mvnHome}/bin/mvn  package"
    }
    
    }
