pipeline {
    agent any
    
    stages {
        stage('Check Fibonacci') {
            steps {
                script {
                    def number = 13 // Change this to the number you want to check
                    
                    // Function to check if a number is Fibonacci
                    def isFibonacci = { num ->
                        def a = 0, b = 1
                        while (b < num) {
                            def temp = b
                            b += a
                            a = temp
                        }
                        return b == num
                    }
                    
                    // Check if the given number is Fibonacci
                    if (isFibonacci(number)) {
                        echo "${number} is in the Fibonacci sequence"
                    } else {
                        echo "${number} is not in the Fibonacci sequence"
                    }
                }
            }
        }
    }
}
