pipeline {
     agent {
        docker { image 'kamasubb/conda-forge-linux-anvil-ppc64le' }
          }
    stages {
        stage('Test') {
            
           
            steps {
                echo 'Building..'
                sh 'yum install -y wget openssh-clients bzip2'
                sh 'wget https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh'
                sh 'sh Miniconda3-latest-Linux-x86_64.sh -b -p /opt/conda  -u'
                sh '/opt/conda/bin/conda install -y conda-build' 
                sh '/opt/conda/bin/conda build recipe'
                
            }
        }
    }
}
