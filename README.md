# Introduction

Microservice를 개발 후 Container 기반으로 배포하여 개발/테스트/운영하는 경우가 점차 늘어가고 있습니다. 본 실습은 이 과정에서 필요한 Registry, Kubernetes, CI/CD 툴을 각각 OCI Regsitry, OKE(OCI Container Engine for Kubernetes), Wercker를 사용하여 Container 기반 배포 자동화를 경험해 보는 것을 목표로 합니다.


# 사전 준비 사항 

실습을 위해서는 아래 계정이 필요합니다. 계정이 없으신 경우 아래 링크를 이용해 계정을 생성합니다.

  - [GitHub 계정](https://github.com/join)
  - [Wercker 계정](https://app.wercker.com)
      * GitHub 계정으로 만들면 됩니다.
  - [Oracle Cloud Trial](https://cloud.oracle.com)
      * 강사에게 이메일을 알려주고 등록하면 다음 URL에서 실습용 Oracle Cloud 접속 정보를 확인할 수 있습니다.<br>
      http://129.213.20.158:7001/CloudAccount/account-info.jsp 

# 실습내용

## Lab 100 - Microservice를 개발
서비스를 개발하여 소스관리툴에 반영하는 것을 가정하여 여기서는 이미 개발된 소스를 각자의 GitHub 계정으로 복제합니다.

  - [Lab 100으로](Lab100.md)


## Lab 200 - Wercker를 통한 빌드 자동화
소스 변경으로 인해 Git에 Commit이 발생하면 빌드되는 과정으로 Docker Image 생성 및 OCI Registry에  등록하는 과정을 실습합니다

  - [Lab 200으로](Lab200.md)


## Lab 300 - Kubernetes 환경 설정
사용할 Kubernetes를 OCI 환경의 Kubernetes 클러스터를 구성하고 클라이언트에서 kubectl로 작업하기 위해서는 환경 설정 작업이 필요합니다. 이 부분에 대해서 실습합니다.<br>
**실습 편의성을 위해 이미 구성된 환경인 옵션 #1로 진행합니다.직접 해보기를 원하시는 분은 옵션 #2로 따라해 보시기 바랍니다.**

  - **옵션 #1. 구성된 환경 사용 & 로컬 kubectl 환경만 구성하기 [Lab 300-1으로](Lab300-1.md)**
  - 옵션 #2. 모든 과정 직접 해보기 [Lab 300-1으로](Lab300-2.md)  


## Lab 400 - Wercker를 통한 배포 자동화
소스 변경으로 인해 Git에 Commit이 발생하면 빌드이후 배포되는 과정으로 Registry에 등록된 Image를 Kuberneted(OKE)에 배포하는 것 까지 실습합니다.

  - [Lab 400으로](Lab400.md)

# 참고 
  - [Container Native Development with OKE Workshop](https://oracle.github.io/learning-library/workshops/container-native-development-with-oke/?page=README.md)