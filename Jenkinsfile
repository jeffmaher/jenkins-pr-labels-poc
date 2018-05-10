enum VersionIncrements { MAJOR, MINOR, PATCH } 

labels_str = '["major", "oogabooga", "etc"]'

def getLabel(){
        if(labels_str == null) {
            return
        }

        labels = readJSON text: labels_str
        versionIncrement = null

        if labels.contains("major") VersionIncrements.MAJOR
        else if labels.contains("minor") VersionIncrements.MINOR
        else if labels.contains("patch") VersionIncrements.PATCH
}

node {
    stage('Build') {
        echo "Label: ${getLabel()}"
    }
}
