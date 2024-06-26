# 오픈소스SW개론

 ## TOP 명령어
 **▶ linux에서 시스템을 모니터링하는 명령어**

##### 사용법: `$ top [option]`
 
 ### 1. 요약 영역
 * top 명령어는 현재 OS의 상태를 나타내주는 CLI 어플리케이션
 * top에서 상단에 위치
 * 전체 프로세스가 OS에 대해서 리소스를 어느정도 차지하고 있는지를 알려줌

| System time | uptime | user sessions | Load Average |
|---|---|---|---|

| Tasks |
|---|

| CPU |
|---|

| Memory |
|---|
   
 ### 2. 시스템 현재 시간, OS가 살아있는 시간, 유저 세션수 (System time, uptime and user sessions)
 * 각각 시스템의 현재 시간, OS가 얼마나 살아있는지, 현재 접속중인 유저 세션 수를 나타냄

 ### 3. 로드 애버리지(Load Average)
 * CPU Load의 이동 평균를 표시
 
 ### 4. Tasks
 * 현재 프로세스들의 상태를 나태내주는 영역
 
 ### 5. CPU 사용량
 *  CPU가 어떻게 사용되고 있는지 그 사용율을 보여주는 영역
   
 ### 6. 메모리 사용량
 * total : 총 메모리 양
 * free : 사용가능한 메모리 양
 * used : 사용중인 메모리 양
   
 ### 7. 디테일 영역
 * PID 프로세스 ID이며 프로세스를 구분하기 위한 겹치지않는 고유한 값
 * USER 해당 프로세스를 실행한 USER 이름 또는 효과를 받는 USER의 이름
 * PR & NI    
    PR : 커널에 의해서 스케줄링되는 우선순위  
    NI : PR에 영향을 주는 nice라는 값     
 * VIRT, RES, SHR, %MEM    
     VIRT : 프로세스가 소비하고 있는 총 메모리입니다. 프로그램이 실행중인 코드, heap, stack과 같은 메모리, IO buffer 메모리를 포함  
     RES : RAM에서 사용중인 메모리의 크기를 나타냄  
     SHR : 다른 프로세스와의 공유메모리(Shared Memory)를 나타냄    
     %MEM : RAM에서 RES가 차지하는 비율을 나타냄  
 * S: 프로세스의 현재 상태를 나타냄  
 * TIME+ : 프로세스가 사용한 토탈 CPU 시간  
 * COMMAND : 해당 프로세스를 실행한 커맨드를 나타냄
--------------------------------
 ## PS 명렁어 
**▶ 현재 실행 중인 프로세스와 상태를 출력하는 명령어**

##### 사용법: `$ ps [option]`


### 명령어 옵션
| 옵션 | 의미 | 
|:---:|:---|
|-a	| 세션 리더와 터미널과 연관이 없는 프로세스를 제외한 모든 프로세스를 출력 |
| a	| BSD 스타일로서 터미널과 연관된 모든 프로세스를 출력하거나,   x 옵션과 함께 사용되어 모든 프로세스를 출력 |
| -d	|세션 리더를 제외한 모든 프로세스들을 출력 |
| r	| 실행 프로세스만 출력 |
| x	| BSD 스타일로서 혼자 사용되면 사용자에 의해 소유된 모든 프로세스를 출력하고 a 옵션과 함께 사용되어 모든 프로세스를 출력 |
| -l	| 상세한 내용을 출력 |
| -f	| 완전한 형식의 목록을 출력 |
| -h	| 메뉴를 보여주지 않음(PID, TTY, STAT, TIME, COMMAND 등) |
| -j	| 작업에 관련된 ID를 출력 | 
| -l	| -j 옵션보다 자세하게 정보를 출력 | 
| u	| 사용자 친화적인 형식으로 출력 |
| f	| 프로세스 간 상속관계를 트리구조로 출력 | 
| n	| 사용자의 정보를(모든 형식의 UID와 GID를 포함하여) 숫자로 표시 |
| -w	| 출력결과를 생략하지 않고 넓게 출력 |

### 출력 의미
| 필드 | 의미 | 
|:---:|:---|
PID(process ID)	| 프로세스마다 주어지는 번호
TTY(TeleTypewriter) |	명령어가 실행되는 터미널의 번호, 할당된 것이 없는 경우 물음표(?) 출력
STAT	| 실행되고 있는 프로세스 상태(R, S, D, T, Z, W, N)
START	| 프로세스가 시작된 시간
TIME	| CPU가 사용한 시간
USER(USER)	| 사용자 이름
COMMAND(COMMAND)	| 사용자가 실행한 명령어
UID(User ID)	| 사용자의 ID
PGID(Parent Group ID)	| 사용자 부모 프로세스이 그룹 ID
SID(Session ID)	| 세션 ID
PRI(PRIority)	| 실행하는 우선순위에 따른 프로세스
NI(NIce)	| nice에 의한 우선순위에 따른 프로세스
RSS(Resident Set Size)	| 프로세스가 사용하는 메모리의 크기
SZ(SiZe)	| 프로세스가 사용하는 자료와 스택의 크기
SHRD(SHareD)	| 프로세스가 사용하는 공유 메모리
%CPU	| 프로세스가 사용하는 CPU 점유율
%MEM	| 프로세스가 사용하고 있는 메모리 점유율
WCHAN	| 프로세스가 실행하고 있는 커널 루틴
VSZ	| KiB 단위(1024 바이트 단위)의 프로세스의 버추얼 메모리 크기(vsize와 동일한 의미)


#### ※ps와 top의 차이점  
- ps: ps한 시점에 proc에서 검색한 cpu 사용량  
- top: proc에서 일정 주기로 합산해 cpu 사용율 출력
 --------------------------
 ## JOBS 명렁어

 **▶ 백그라운드로 실행된 프로그램이나 "Ctrl + z"를 입력하여 실행한 프로그램에 대해서 확인하는 명령어**

##### 사용법 : `$ jobs [option]`
 
 ### 명령어 옵션
| 옵션 | 의미 | 
|:---:|:---|
-p	| 백그란운드에 있는 프로세스의 프로세스 아이디(PID)만 출력
-l	| 백그라운드에 있는 프로세스의 프로세스 아이디(PID)를 함께 출력
-s	| 백그라운드에 있는 프로세스 중 멈춰있는 프로세스만 출력
-r	| 백그라운드에 있는 프로세스 중 실행중인 프로세스만 출력


 ----------------------------
 ## KILL 명령어 
**▶ 프로세스를 종료하는 명렁어**

##### 사용법: `$ kill [option] <PID>`

### 명령어 옵션
| 옵션 | 의미 |
|:---:|:---|
-s <signal> | 특정 시그널(signal)을 사용하여 프로세스를 종료, 기본적으로 SIGTERM 시그널이 사용
-l, --list | 지원되는 시그널(signal) 목록을 출력
-a, --all | 현재 사용자에 속한 모든 프로세스를 종료
-q, --queue | 프로세스에 시그널을 보내는 대신 시그널을 대기열에 추가

`$ kill -9 <PID>` : SIGKILL 시그널을 사용하여 강제로 프로세스를 종료, 이는 프로세스를 멈추는 가장 강력한 방법이지만 데이터 손실이 발생할 수 있음

### 명령어 장단점
장점:   
- 간단한 명령어로 빠르게 프로세스를 종료할 수 있음
- 다양한 옵션을 사용하여 프로세스 동작을 제어할 수 있음

단점:  
- 잘못 사용하면 의도치 않은 프로세스 종료가 발생할 수 있음
- SIGKILL 시그널을 사용하여 강제 종료할 경우 프로세스가 올바르게 정리되지 않을 수 있고 데이터 손실 등의 문제가 발생할 수 있음
 
