pipeline {
    agent any
   
    stages {
        stage('Checkout') {
            steps {
                // Checkout the source code from the repository
                git branch: 'main', url:'https://github.com/shravanikodam01/multipage-website-CC-inClassLab3.git'
            }
        }
       
        stage('Build') {
            steps {
                // Assuming your HTML file is at the root of the repository
                sh 'cp index.html build/'  // Copy the HTML file to a build directory (adjust as needed)
            }
        }
       
        stage('Test') {
            steps {
                // Add commands to run any tests (for simplicity, we skip tests in this example)
                echo 'Skipping tests for a simple HTML file.'
            }
        }
       
        stage('Deploy') {
            steps {
                // Assuming you want to deploy the HTML file to a web server
                // You might use a tool like rsync, scp, or any other deployment method
                echo 'Deploying the HTML file...'
                // Add your deployment command here
                // For example, you could use rsync to copy the files to a server:
                // sh 'rsync -avz build/ user@your-server:/path/to/deployment/'
            }
        }
    }
}
