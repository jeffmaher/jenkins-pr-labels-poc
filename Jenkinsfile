import groovy.json.JsonSlurper

jsonSlurper = new JsonSlurper()

enum VersionIncrements { MAJOR, MINOR, PATCH } 

pipeline {
    agent any

    stages {
        stage('Build Version Tagged Image') {
            steps {                           
                if(labels == null) {
                    return
                }
                
                labels = jsonSlurper.parseText(env.pull_request_labels)
                versionIncrement = null
                for(label in labels){
                    switch(label) {
                        case "major":
                            break                    
                        case "minor":
                            break
                        case "patch":
                            break
                    }
                
                    if(versionIncrement != null) {
                        break
                    }
                }
                echo "Build Type: ${versionIncrement.value}"
            }
        }
    }
}
