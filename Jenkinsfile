
pipeline {
    agent any

    stages {
        stage('Checkout Katalon Project') {
            steps {
                echo 'Katalon project checked out successfully.'
            }
        }

        stage('Run Katalon Test') {
            steps {
                bat '''
                "D:\\Katalon_Studio_Engine_Windows_64-11.6.0\\Katalon_Studio_Engine_Windows_64-11.6.0\\katalonc.exe" ^
                -noSplash ^
                -runMode=console ^
                -projectPath="%WORKSPACE%\\Make-Appointment-Katalon-Project.prj" ^
                -testSuitePath="Test Suites/NewtestMakeapp" ^
                -executionProfile="default" ^
                -browserType="Chrome"
                '''
            }
        }
    }
}
