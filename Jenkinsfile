enum VersionIncrements { MAJOR, MINOR, PATCH } 

labels_str = '["major", "oogabooga", "etc"]'

def getLabel(){
        script {
            if(labels_str == null) {
                return
            }

            jsonSlurper = new groovy.json.JsonSlurper()
            labels = jsonSlurper.parseText(labels_str)
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
        echo 'Label: ${getLabel()}'
    }
}
