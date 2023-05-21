# 1 dltkdals



# ps(process status)
현재 실행중인 프로세스 목록과 상태를 보여준다.


$ ps [option]
## 옵션
$ps -ef :모든 프로세스를 풀 포멧으로 출력
$ps -ef | grep '프로세스 명' : '프로세스 명'의 프로세스를 구동 확인함.
$ps -aux: 실행중인 모든 프로세스 확인
$ps auxf : 실행중인 프로세스를 트리구조로 보여줌
$ps auxfww : 실행중인 프로세스를 트리구조 + 모든 실행중인 옵션 확인가능


# 2 top
리눅스 시스템의 운용상황을 실시간으로 전반적인 상황을 모니터링하거나 프로세스 관리를 할 수 있는 유틸리티이다.
## 옵션
top shift + p : CPU 사용률 내림차순
top shit + m : 메모리 사용률 내림차순
top shift + t : 프로세스가 돌아가고 있는 시간 순
top -k : kill. k 입력 후 PID 번호 작성. signal은 9
top -f : sort field 선택 화면 -> q 누르면 RES순으로 정렬
top -a : 메모리 사용량에 따라 정렬
top -b : Batch 모드로 작동
1 : CPU Core별로 사용량 보여줌

 ps 와 top의 차이점 
    * ps는 ps한 시점에 proc에서 검색한 cpu 사용량이다.
    * top은 proc에서 일정 주기로 합산해서 cpu 사용율을 출력한다. 


# 3 jobs
백그라운드로 실행되는 작업목록(작업번호, 상태, 명령어)을 보여주는 리눅스 명령어


$jobs [옵션] [job ID]
## 옵션
jobs -x command [args]
-l:프로세스 그룹 ID를 state필드 앞에 출력
-n: 프로세스 그룹중에 대표 프로세스 ID를 출력
-p:각 프로세스 ID에 대해 한 행씩 출력
command: 지정한 명령어를 실행 


# 4 kill
프로세스에 특정한 signal을 보내는 명령어이다.
일반적으로 종료되지 않는 프로세스를 종료시킬 때 많이 사용한다.


$kill [옵션] [PID]
##옵션

-9:	프로세스아이디(PID)를 직접 지정하여 종료시 사용 됩니다
-l:	신호(Signal)로 사용할 수 있는 신호(Signal) 이름들을 보여준다
