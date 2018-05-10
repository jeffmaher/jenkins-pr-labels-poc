enum VersionIncrements { MAJOR, MINOR, PATCH } 

labels_str = '["major", "oogabooga", "etc"]'

/**
* Dev Notes:
* Requires:
* - Pipeline Utility Steps Jenkins Plugin
* - Approval to use:
    - new java.util.LinkedHashMap
    - staticMethod org.codehaus.groovy.transform.ImmutableASTTransformation checkPropNames java.lang.Object
    - java.util.Map
*/
def getLabel(){
        versionIncrement = null
        
        if(labels_str == null) {
            return
        }

        labels = readJSON text: labels_str
        for(label in labels){
            switch(label) {
                case "major":               
                case "minor":
                case "patch":
                    versionIncrement = VersionIncrements.valueOf(label)
            }

            if(versionIncrement != null) {
                return versionIncrement
            }
        }
}

node {
    stage('Build') {
        echo "Label: ${getLabel()}"
    }
}
