pipeline {
    agent any

    stages {
        stage('DiskSpace') {
            steps {
                echo 'Building..'
			    sh '''#!/bin/bash
                df -h
                '''	
            }
        }
        stage('Uptime') {
            steps {
                echo 'Uptime..'
			    sh '''#!/bin/bash
                uptime
                '''	
            }
        }
        stage('patching') {
            steps {
                echo 'Deploying....'
                echo 'Uptime..'
			    sh '''#!/bin/bash
                sudo apt-get update -y
                '''	
            }
        }
        stage('Uptime-2') {
            steps {
                echo 'Checking Post Patch uptime....'
                echo 'Uptime..'
			    sh '''#!/bin/bash
                uptime
                '''	
            }
        }
        stage('Mount') {
            steps {
                echo 'Mounting Filesystem....'
                echo 'Uptime..'
			    sh '''#!/bin/bash
                sudo mount -a
                '''	
            }
        }        
    }
}
