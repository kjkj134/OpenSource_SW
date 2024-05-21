# OpenSource_SW

 ## TOP 명령어
 **linux에서 시스템을 모니터링하는 기본적인 명령어인 top**
 
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
 
 ### 4. Tasks: Tasks
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


#### ※ps와 top의 차이점  
- ps는 ps한 시점에 proc에서 검색한 cpu 사용량  
- top은 proc에서 일정 주기로 합산해 cpu 사용율 출력
 --------------------------
 ## JOBS 명렁어


 
 ----------------------------
 ## KILL 명령어 


 
