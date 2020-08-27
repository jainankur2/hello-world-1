def ENVIRONMENTS = [
    'DEV (EMEA)': [env: 'cm-dev', vf_region: 'emea', aws_region: 'eu-west-1'],
    'QA (EMEA)': [env: 'cm-qa', vf_region: 'emea', aws_region: 'eu-west-1'],
    'PROD (EMEA)': [env: 'cm-prod', vf_region: 'emea', aws_region: 'eu-west-1'],
]

def allowed_environments = get_environments(ENVIRONMENTS, env.JOB_NAME)





pipeline {
      agent any
      parameters {
        choice(name: 'ENVIRONMENT', choices: allowed_environments, description: 'The environment.')
        password(name: 'AWS_CREDENTIALS', defaultValue: '', description: 'Enter AWS credentials. e.g. export AWS_ACCESS_KEY_ID=[...] export AWS_SECRET_ACCESS_KEY=[...] export AWS_SESSION_TOKEN=[...]')
    }

      stages{
         stage('Build artifact'){
            steps{
              sh 'echo "build"'
            }
             }
         stage('deploy'){
             steps{
                sh 'echo "deploy"'
              }
         }        

      }

}
