enum VersionIncrements { MAJOR, MINOR, PATCH } 

labels_str = '["major", "oogabooga", "etc"]'

/**
* Dev Notes:
* Requires:
* - Pipeline Utility Steps Jenkins Plugin
* - Approval to use java.util.LinkedHashMap
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
