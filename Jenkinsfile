import groovy.json.JsonSlurper


node {
    stage('Build') {
        echo 'Hello'
    }
}




// jsonSlurper = new JsonSlurper()

// enum VersionIncrements { MAJOR, MINOR, PATCH } 

// def getLabel(){
//         script {
//             if(labels == null) {
//                 return
//             }

//             labels = jsonSlurper.parseText(env.pull_request_labels)
//             versionIncrement = null
//             for(label in labels){
//                 switch(label) {
//                     case "major":
//                         break                    
//                     case "minor":
//                         break
//                     case "patch":
//                         break
//                 }

//                 if(versionIncrement != null) {
//                     return versionIncrement
//                 }
//             }
//         }
// }

// pipeline {
//     agent any

//     stages {
//         stage('Build Version Tagged Image') {
//             steps {
//                 versionIncrement = getLabel()
//                 echo "Build Type: ${versionIncrement.value}"
//             }
//         }
//     }
// }
