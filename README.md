#### 20202873_양승유_README숙제

+ linux command
1) top: 실시간 **cpu 사용량**을 체크해주는 도구이다. 리눅스를 사용하는 디바이스의 성능이나 리눅스 서버의 성능 체크할 때 매우 유용하다.
어떤 프로세스가 cpu를 과다하게 잡고 있는지 분석이 가능하다.
   
   |표시|설명|
   |---|---------|
   |XX:XX:XX|현재 서버의 시간을 나타낸다|
   |n user|n명의 사용자 접속을 나타낸다|
   |load average|부하율을 표시한다|
   
   |task|설명|
   |---|---------|
   |total|총 가동되는 프로세스의 수| 
   |n running|총 n개의 프로세스가 실행 중임|
   |n sleeping|총 n개의 프로세스가 대기 중임| 
   |n stopped|n개의 프로세스가 멈춤 상태임|
   |n zombie|n개의 프로세스가 좀비 상태에 있음|
   
   |CPU|설명|
   |---|---------|
   |%us|유저 레벨에서 사용하고 있는 cpu비중|
   |%sy|시스템 레벨에서 사용하고 있는 cpu비중|
   |%id|유후 상태의 cpu비중|
   |%wa|시스템이 I/O 요청을 처리하지 못한 상태에서의 cpu idle 상태인 비중|
   
   |메모리|설명|
   |---|---------|
   |n total|전체 물리적인 메모리|
   |n used|사용중인 메모리|
   |n free|사용되지 않은 여유 메모리(free memory)|
   |n buffers|버퍼된 메모리|
   
   |Swap|설명|
   |---|---------|
   |n total|전체 스왑 메모리|
   |n used|사용중인 스왑 메모리|
   |n free|남아있는 스왑 메모리|
   |n cached|캐싱 메모리|
   
   |프로세스 상태|설명|
   |---|---------|
   |PID|프로세스 ID (PID)|
   |USER|프로세스를 실행시킨 사용자 ID|
   |PRI|프로세스의 우선순위 (priority)|
   |NI|NICE값. 일의 nice value 값으로, 마이너스를 가지는 nice value가 우선순위가 높음|
   |VIRT|가상 메모리의 사용량(SWAP + RES)|
   |RES|현재 페이지가 상주하고 있는 크기 (Resident Size)|
   |SHR|분할된, 페이지 프로세스에 의해 사용된 메모리를 나눈 메모리의 총합|
   |S|프로세스의 상태S-Sleeping, R-Running, W-Swapped out process, Z-Zombies|
   |%CPU|프로세스가 사용하는 CPU 사용률|
   |%MEM|프로세스가 사용하는 메모리 사용률|
   |COMMAND|실행된 명령어|
   
   |top 실행 후 명령어|설명|
   |---|---------|
   |Shift + p|CPU 사용률이 높은 프로세스 순서대로 표시|
   |Shift + m|메모리 사용률이 높은 프로세스 순서대로 표시|
   |Shift + t|프로세스가 돌아가고 있는 시간 순서대로 표시|
   |-k|프로세스 kill, -k입력 후 종료할 PID 입력. signal을 입력하라고 하면 kill signal인 9를 입력|
   |-a|메모리 사용률에 따라 정렬|
   |-b|batch 모드 작동|
   |-c|명령행/프로그램 이름 토글|
   |-d|지연 시간 간격은 다음과 같다. ss.tt (seconds.tenths)|
   |-h|도움말|
   |-H|쓰레드 토글|
   |-i|유휴 프로세스 토글|
   |-m|VIRT/USED 토글|
   |-M|메모리 유닛 탐지|
   |-n|반복 횟수 제한|
   |-P|PID를 다음과 같이 모니터: -PN1 -PN2 ...|
   |-s|보안모드 작동|
   |-S|누적 시간 모드 토글|
   |-u|사용자별 모니터링|
   |-U|사용자별 모니터링|
   |-v|version 표시|
   |space bar|refresh|
   |1(숫자 1)|cpu core별로 사용률을 보여줌|
   
   ![linux_top](https://user-images.githubusercontent.com/104362407/170895791-e203ca61-81f0-42f5-b2b3-e3bd57411a1f.png)

   
2) 
