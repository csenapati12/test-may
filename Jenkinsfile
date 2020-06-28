node(){
stage('clone'){
checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/csenapati12/test-may.git']]])
}


stage('modify'){
sh"""
sed -i 's/version: ".*"/version: "0.0.9"/g' test.json
"""
}
}
