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
            echo "========always========"
        }
        success{
            echo "========pipeline executed successfully ========"
        }
        failure{
            echo "========pipeline execution failed========"
        }
    }
}