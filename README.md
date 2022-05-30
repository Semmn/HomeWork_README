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
   
   [top](https://ironmask84.tistory.com/355)

***   
   
2) ps (Process Status) : 현재 돌아가고 있는 **프로세스**를 확인할 수 있는 리눅스 명령어이다. ps명령어는, os에 따라 결과가 다르게 나타나고 표기법에도 차이를 보인다.
옵션 사용 시에 System V 계열은 대시 (dash, -)를 사용하고 BSD 계열은 대시(-)를 사용하지 않는다. GNU에서는 옵션 표기에서 두 개의 대시(--)를 사용한다.

   |옵션|설명|
   |:---|---------:|
   |-A|모든 프로세스를 출력한다|
   |a(BSD)|터미널과 연관된 프로세스를 출력하는 옵션이다. 보통 x옵션과 연계하여 모든 프로세스를 출력할 때 사용한다|
   |-a|세션 리더(일반적으로는 로그인 셀)을 제외하고 데모 프로세스처럼 터미널에 종속되지 않는 모든 프로세스를 출력한다|
   |-c|커널 프로세스를 제외한 모든 프로세스를 출력해 준다|
   |-f|풀 포맷으로 보여준다. 유닉스 스타일로 출력해주는 옵션으로 UID, PID, PPID등이 함께 표시된다|
   |-l(System V)|긴 포맷으로 보여준다|
   |l(BSD)|프로세스의 정보를 길게 보여주는 옵션으로 우선순위와 관련된 PRI와 NI 값을 확인할 수 있다|
   |-o|출력 포맷을 지정하는 옵션으로, 값으로는 pid, tty, time, cmd등을 지정할 수 있다|
   |-M|64비트 프로세스들을 보여준다|
   |-m|프로세스들 뿐만 아니라 커널 쓰레드들도 보여준다|
   |-p|특정 PID를 지정할 때 사용한다|
   |-r|현재 실행 중인 프로세서를 보여준다|
   |u(BSD 계열)|프로세스의 소유자를 기준으로 출력한다|
   |-u|특정 사용자의 프로세스의 정보를 확인 할 때 사용한다. 사용자를 지정하지 않으면 현재 사용자를 기준으로 정보를 출력한다|
   |x(BSD 계열)|데몬 프로세스처럼 터미널에 종속되지 않은 프로세스를 출력한다. 보통 a옵션과 결합하여 모든 프로세스를 출력할 때 사용한다.|
   |-x|로그인 상태에 있는 동안 아직 완료되지 않은 프로세서를 보여준다. 유닉스 시스템은 사용자가 로그아웃한 후에도 임의의 프로세스가 계속동작하게 할 수 있다.
   ||그러면 그 프로세스는 자신을 실행시킨 셀이 없어도, 계속 자신의 일을 수행하는데 이러한 프로세스는 일반적인 ps명령으로 확인 불가능하다. 이 때 -x옵션을 사용하면 자신의|
   ||터미널이 없는 프로세서들을 확인할 수 있다.|

   ps명령어만 단독으로 사용했을 경우: 사용자와 관련된 프로세스를 출력해준다. ps는 이렇게 단독적으로 사용되기 보다는 거의 옵션으로 같이 사용되는 경우가 많다.
   기본적으로 PID,TTY,TIME,CMD 이렇게 네 가지 정보가 출력된다.
   
   |ps항목|설명|
   |---|---------|
   |USER|BSD 계열에서 나타나는 항목으로 프로세스 소유자의 이름을 표시한다|
   |UID|SYSTEM V계열에서 나타내는 항목으로 프로세스 소유자의 이름을 표시한다|
   |PID|프로세스의 식별번호|
   |PPID|부모 프로세스 ID|
   |y.CPU|CPU사용 비율의 추정치(BSD)|
   |y.MEM|메모리의 사용 비율의 측정치(BSD)|
   |VSZ|k단위 또는 페이지 단위에서 가상메모리 사용량|
   |RSS|실제 메모리의 사용량(Resident Set Size)|
   |TTY|프로세스와 연결된 터미널|
   |S.STAT|현재 프로세스의 상태 코드(S: SYSTEM V, STAT: BSD)|
   |TIME|총 CPU 사용시간|
   |COMMAND|프로세스의 실행 명령행|
   |STIME|프로세스가 시작된 시간 혹은 날짜|
   |C, CP|짧은 시간 동안의 CPU 사용률(C : SYSTEM V, CP: BSD)|
   |F|프로세스의 플래그|
   |PRI|실제 실행 우선순위|
   |NI|nice 우선순위 번호|
   
   ![linux_ps_all](https://user-images.githubusercontent.com/104362407/170896649-822d3125-37bc-42aa-ab59-8a092992c394.png)
   
   [ps](https://jhnyang.tistory.com/268)
   
***

3) jobs: jobs 명령어는 **작업의 상태**를 표시하는 명령어이다. 현재 쉘 세션에서 실행시킨 백그라운드 작업의 목록이 출력되며, 각 작업하는 번호가 뭍어 있어 kill 명령어 뒤에
"%번호"등으로 사용할 수 있다.

   백그라운드 작업의 상태값

   |상태|설명|
   |---|---------|
   |Running|작업이 계속 진행중임|
   |Done|작업에 완료되어 0을 반환|
   |Done(Code)|작업이 종료되었으며, 0이 아닌 코드를 반환|
   |Stopped|작업이 일시 중단됨|
   |Stopped SIGTSTP|SIGTSTP 시그널이 작업을 일시 중단시킴|
   |Stopped SIGSTOP|SIGSTOP 시그널이 작업을 일시 중단시킴|
   |Stopped SIGTTIN|SIGTTIN 시그널이 작업을 일시 중단시킴|
   |Stopped SIGTTOU|SIGTTOU 시그널이 작업을 일시 중단시킴|

   |옵션|설명|
   |---|---------|
   |-l|프로세스 그룹 ID를 State 필드 앞에 출력|
   |-n|프로세스 그룹 중에 대표 프로세스 ID를 출력|
   |-p|각 프로세스 ID에 대해 한 행씩 출력|
   |command|지정한 명령어를 실행|

   [jobs](https://hbase.tistory.com/265)

***

4) kill: 프로세스에 **시그널**을 보내는 명령어이다. kill -l을 통해 kill 시그널 리스트를 확인가능하다.

|주요 시그널|영어|설명|
|---|------|---------|
|1) SIGHUP|hang up|세션이 종료될 때 시스템이 내리는 시그널|
|2) SIGINT|Interrupt|Ctrl + c, 종료 요청 시그널|
|3) SIGQUIT|QUIT|키보드로부터 오는 실행 중지 시그널|
|4) SIGILL|ILL|illegal instruction의 약자. 잘못된 명령어를 사용했을 때 발생함|
|5) SIGTRAP|TRAP|trace(추적), breakpoint(중지점)에서 TRAP가 발생할 때|
|6) SIGABRT (ABRT)|abort|비정상종료 함수에 의해 발생함|
|7) SIGBUS||메모리 접근 에어리 발생하는 시그널|
|9) SIGKILL|kill|강제 종료 시그널
|11) SIGSEGV|Segment Violation|메모리 침범이 일어날 때 시스템이 내보내는 시그널|
|15) SIGTERM|TERM|Terminate의 약자로 가능한 정상 종료시키는 시그널로 kill명령의 기본 시그널이다|
|17) SIGCHLD|child|자식 프로세스가 stop되거나 종료되었을 때 부모에게 전달되는 신호|
|18) SIGCONT(CONT)|Continue|STOP 시그널에 의해 정지된 프로세스를 다시 실행 시킬 때 사용됨|
|19) SIGSTOP (STOP)|STOP|터미널에서 입력된 정지 시그널. SIGCONT로 재실행시킬 수 있음|
|20) SIGTSTP|Temporary Stop|Ctrl+z 일시 중지 요청 시그널|
|29) SIGIO|I/O|비동기 입출력이 발생했을 경우|

![linux_kill](https://user-images.githubusercontent.com/104362407/170897253-263aff0b-95ed-4707-abdd-a9c27f4223eb.png)

[kill](https://frogand.tistory.com/69)
[kill2](https://jhnyang.tistory.com/143)

***



