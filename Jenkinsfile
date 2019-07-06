pipeline {
  agent any
  stages {
    stage('Get_Sources') {
      agent {
        node {
          label 'min-centos-7'
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