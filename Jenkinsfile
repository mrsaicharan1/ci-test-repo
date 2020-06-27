node('master') {
   stage('Source Code') {
       git "https://github.com/mrsaicharan1/Beginning-Jenkins"
   }
   
   dir('Lesson5') {
      printMessage('running pipeline')
      stage('Run unit tests') {
          sh 'python3 test_functions.py'   
      }
      printMessage('testing complete')
      stage('Deployment') {
          if(env.BRANCH_NAME == 'master') {
              printMessage('Deploying Master Branch')
              
          }
          else {
              printMessage('No deployment configured for this branch')
          }
      }
       
   }
}

def printMessage(message) {
    echo "${message}"
}

