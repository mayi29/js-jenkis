pipeline{
    agent any
    stages{
        stage("Build"){
            steps{
                echo "====++++ executing Build... ++++===="
                sh 'npm install'
            }
            post{
                always{
                    echo "====++++ Build Finished! ++++===="
                }
                success{
                    echo "====++++ Build executed succesfully! :) ++++===="
                }
                failure{
                    echo "====++++ Build execution failed :( ++++===="
                }
        
            }
        }
        stage("Test"){
            steps{
                echo "====++++ executing Test... ++++===="
                sh 'npm test'
            }
            post{
                always{
                    echo "====++++ Test finished! ++++===="
                }
                success{
                    echo "====++++ Test executed succesfully ++++===="
                }
                failure{
                    echo "====++++ Test execution failed ++++===="
                }
        
            }
        }
        stage("Deploy"){
            steps{
                echo "====++++ executing Deploy... ++++===="
                sh 'nohup npm start > output.log &'
            }
            post{
                always{
                    echo "====++++ Deploy Finished! ++++===="
                }
                success{
                    echo "====++++ Deploy executed succesfully ++++===="
                }
                failure{
                    echo "====++++ Deploy execution failed ++++===="
                }
        
            }
        }
    }
    post{
        always{
            echo "======== pipeline finished! ========"
        }
        success{
            echo "========pipeline executed successfully ========"
        }
        failure{
            echo "========pipeline execution failed========"
        }
    }
}