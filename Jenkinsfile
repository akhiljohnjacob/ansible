pipeline {
    agent any

    options {
        overrideIndexTriggers(false)
    }

    parameters {
        string(
            name: 'ENVIRONMENT',
            defaultValue: 'dev',
            description: 'Environment to deploy'
        )

        choice(
            name: 'ACTION',
            choices: ['build', 'deploy', 'rollback'],
            description: 'Select the action to perform'
        )

        booleanParam(
            name: 'RUN_TESTS',
            defaultValue: true,
            description: 'Run automated tests?'
        )
    }

    stages {
        stage('Show Parameters') {
            steps {
                echo "Environment: ${params.ENVIRONMENT}"
                echo "Action: ${params.ACTION}"
                echo "Run Tests: ${params.RUN_TESTS}"
            }
        }
    }
}
