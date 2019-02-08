# git_sample
git 사용 설명을 위한 브랜치입니다.


사용 규칙
1. 절대 master 브랜치에서 작업하지 않는다.

2. 작업 브랜치는 master에서 생성

   ex) job_0001
   
3. 테스트 진행시 작업 브랜치를 stg 브랜치에 머지하여 진행

   ※ 절대 stg 브랜치를 작업 브랜치에 머지하지 않는다. (작업자가 의도하지 않은 코드가 작업브랜치에 머지되어 사고 발생 100%)
   
4. 테스트 완료된 작업 브랜치를 master 브랜치에 머지하여 진행

5. 운영 배포전까지 크게 충돌나는 것을 방지하기 위해 중간중간 master브랜치를 작업브랜치에 머지한다.

   ※ master 머지전에는 작업브랜치에 master를 머지하는 것을 추천. (master가 더러워지는 것보다는 작업브랜치가 더러워지는 것이 나음)
   
6. 충돌 발생시 최근 작업자와 함께 충돌을 해결한다.

7. 배포시 배포 tag를 업데이트하여, 어디까지 배포하였는지 표기

   tag REAL_LATEST, tag STG_LATEST
   
