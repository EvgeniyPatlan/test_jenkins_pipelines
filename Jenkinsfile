pipeline {
  agent {
    docker {
      image 'centos.centos7'
    }

  }
  stages {
    stage('Get_Sources') {
      agent {
        node {
          label 'min-centos-7-x64'
        }

      }
      steps {
        sh '''sudo yum -y install wget
wget https://raw.githubusercontent.com/EvgeniyPatlan/build_scripts/master/pg_patches/ppg-common_builder.sh
mkdir test
bash -x ppg-common_builder.sh --builddir=$PWD/test --get_sources=1'''
      }
    }
  }
}