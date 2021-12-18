pipeline{
    agent none
    stages{
    stage('Non-Parallel Stage'){
        agent{
            label "master"
        }
        steps{
            echo "this stage is executed first"
        }
    }
    stage('Run Tests'){
        parallel{
            stage('Test On windows'){
                agent{
                    label "windows_node"
                }
                steps{
                    echo "Task1 on agent"
                }
            }
            stage('Test on master'){
                 agent{
            label "master"
        }
        steps{
            echo "this stage is executed first"
        }
            }
        }
    }
    }
}
