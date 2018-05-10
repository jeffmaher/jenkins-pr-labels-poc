enum VersionIncrements { MAJOR, MINOR, PATCH } 

/**
* Dev Notes:
* Requires:
* - Pipeline Utility Steps Jenkins Plugin
* - Approval to use:
    - new java.util.LinkedHashMap
    - staticMethod org.codehaus.groovy.transform.ImmutableASTTransformation checkPropNames java.lang.Object
    - java.util.Map
*/
def getLabel(labels_str){
        versionIncrement = null
        
        if(labels_str == null) {
            return
        }

        labels = readJSON text: labels_str
        for(label in labels){
            switch(label) {
                case "major":
                    versionIncrement = VersionIncrements.MAJOR               
                    break
                case "minor":
                    versionIncrement = VersionIncrements.MINOR
                    break
                case "patch":
                    versionIncrement = VersionIncrements.PATCH
                    break
            }

            if(versionIncrement != null) {
                return versionIncrement
            }
        }
}

node {
    stage('Build') {
        if (env.pull_request_action == "closed") {
            echo 'PR Closed'
            echo "Label: ${getLabel(env.pull_request_labels)}"
        }
    }
}
