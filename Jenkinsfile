node(){
properties([parameters([string(defaultValue: '', description: 'Please enter git version', name: 'GIT_VERSION', trim: false)])])
stage('clone'){
checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/csenapati12/test-may.git']]])
}


stage('Change Version'){
 sh"""
       # sed -i 's/version: ".*"/version: "0.2.0"/g' test.json
       sed -i 's/version: ".*"/version: "$params.GIT_VERSION"/g' test.json
       cat test.json
       
 """
}
}
