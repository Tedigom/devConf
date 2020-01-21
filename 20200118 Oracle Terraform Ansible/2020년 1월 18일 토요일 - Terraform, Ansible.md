# 2020년 1월 18일 토요일 - Terraform, Ansible 
Infra as code (IaC) - 코드로 프로비저닝을 하는것. / 스크립트 보다는 선언적(declarative) 코드를 통함.

## Iac Tools - 
1. ad hoc / 
2. Configuration management tools(서버를 프로비저닝 하기 보다는, 소프트웨어(미들웨어 등)을 configuration 하는 것. -chef 등)
3. Server template tools ( docker, packer)
4. Provisioning tool - Terraform -> 말 그대로 provisioning (올리는) 역할을 함.

깃허브에 커밋 -> Jenkins 빌드 -> packer
						-> Ansible
						-> Terraform 

imperative(절차적 ) <-> Declarative(선언적) : 원하는 상태를 선언함 

Ansible -> mutable :  
Terraform -> immutable : 교체를 하는 개념

Immutable <-> mutable
Imperative <-> declarative

===================================================
===================================================

# Terraform
Provisioning declarative
HCL(Hashicorp configuration Language)

Terraform core concept
Resource(조작 가능한 대상의 최소 단위) , 테라폼은 이런 리소스의 CRUD를 담당
Variable (여러곳에 Hard coding하는 것을 막기위해 변수 사용) -> type : string, list, map

Module -> 여러환경에서 재사용성을 재고/ Git 등의 외부저장소 활용
Datasource -> Readonly 성 variable

===================================================
===================================================

# Ansible
다수의 서버를 빠르게 배포, 구성
- 오픈소스 구성관리(configuration management) 프로비저닝 도구(similar to chef, puppet, salt)
- Yaml 형식으로 정의
- agentless
- 멱등성(Idempotency) 

Ansible Inventory : managenode에 대한 호스트 정보를 가지고, 그룹과 호스트로 관리함.

Playbook : Yaml file로 작성
ansible galaxy






