properties([
    parameters([
        gitParameter(name: 'REVISION', 
                     type: 'PT_REVISION',
                     defaultValue: 'master')
    ])
])
    
node {
    echo "Hello World"
    checkout([$class: 'GitSCM',
                          branches: [[name: "${params.REVISION}"]], 
                          doGenerateSubmoduleConfigurations: false, 
                          extensions: [], 
                          gitTool: 'Default', 
                          submoduleCfg: [], 
                          userRemoteConfigs: [[url: 'https://github.com/Omkar29041993/Rollback']]
                        ])  
}
