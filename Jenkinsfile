import groovy.json.JsonSlurper

JSON_SLURPER = new JsonSlurper()
enum VersionIncrements { MAJOR, MINOR, PATCH } 

node {

    stage('Detect Label') {
        if(labels == null) {
            return
        }

        labels = JSON_SLURPER.parseText(env.pull_request_labels)
        versionIncrement = null
        for(label in labels){
            switch(label) {
                case "major":            
                case "minor":
                case "patch":
                    versionIncrement = VersionIncrements.valueOf(label)
            }

            if(versionIncrement != null) {
                break
            }
        }
        echo "Build Type: ${versionIncrement.value}"
    }
}
