enum VersionIncrements { MAJOR, MINOR, PATCH } 

labels_str = '["major", "oogabooga", "etc"]'

def getLabel(){
        if(labels_str == null) {
            return
        }

        labels = readJSON text: labels_str
        versionIncrement = null
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
