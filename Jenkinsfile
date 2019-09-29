#!/usr/bing/env groovy

//Declarative
pipeline {
    agent any    		//agent必需的,告诉Jenkins分配执行器和工作空间	
    stages {			//stage必需的,
		stage('Build') {
			steps {		//step必需的
				echo 'Building....'
				checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/huangwenl/pipeline_test.git']]])\
//				def username = 'Jenkins'
//				echo 'Hello Mr. ${username}'
//				echo "I said, Hello Mr. ${username}"
			}
		}
		stage('Test') {
			steps{
				echo 'Testing....'
			}
		}
		stage('Deploy') {
			steps{
				echo 'Deploying....'
			}
		}
    }
}
