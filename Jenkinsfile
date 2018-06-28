pipeline { 
    agent any  
    tools {
        maven 'maven'
        jdk 'jdk8'
    }
    stages { 
        stage('Initialize') { 
            steps { 
               echo 'Initialie stage started.' 
            }
        }
         stage('test') { 
            steps { 
               echo 'Test stage started.'
               sh 'mvn test'
            }
        }
        stage('package') { 
            steps { 
               echo 'Package stage started.'
               sh 'mvn package'
            }
        }
         stage('Run') { 
            steps { 
               echo 'Run stage started.'
               sh 'mvn exec:java -Dexec.mainClass="com.mrbemafj.multibranch.App'
            }
        }
        stage('Finish') { 
            steps { 
               echo 'Build is finish.'
            }
        }
    }
}
