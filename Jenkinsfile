enum VersionIncrements { MAJOR, MINOR, PATCH } 

def getLabel(){
        script {
            if(env.pull_request_labels == null) {
                return
            }

            jsonSlurper = new groovy.json.JsonSlurper()
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
                    return versionIncrement
                }
            }
        }
}

node {
    stage('Build') {
        echo 'Hello'
    }
}
