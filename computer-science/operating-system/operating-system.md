
### 운영체제의 목적
> 컴퓨터 시스템의 자원을 효율적으로 관리하여 최대한의 성능을 내도록 관리하는 것

1. 효율성
    - 1/N 으로 자원을 분배하지 않고 선택적으로 집중하여 자원을 분배
2. 형평성
    - 효율성만 강조하다보면 차별받는 상황이 생긴다.
3. 편리성
    - 사용자가 편리하게 사용할 수 있도록 동시 사용자, 프로그램이 독자적 컴퓨터에서 수행
    - Multi Tasking: CPU scheduling, 하나의 컴퓨터에서 여러개의 프로그램을 돌린다.

자원
- 하드웨어 자원: cpu, memory    
    - cpu: 빠른 자원
    - memory: 각 프로그램이 조금씩 자원을 가지고있다.
- 소프트웨어 자원: 프로세스, 파일, 메시지 등

운영체제의 분류
1. 동시 작업 가능 여부
    - 단일 작업 single Tasking
        - MS-DOS prompt
        - 이전의 운영체제에서는 한번에 하나만 실행 가능
        - 기능이 제한적이고, 시간 안에 수행하는 것이 중요한 임베디드 소프트웨어 등은 단일작업 OS를 탑재한다.
    - 다중 작업 multi tasking 
        - 현대적인 운영체제, UNIX, MS Windows...
2. 사용자의 수
    - 컴퓨터 한대를 여러 사용자가 '동시에 접속'해서 쓸 수 있는가
    - 단일 사용자 single user
        - MS-DOS, MS Windows (요즘은 서버기능 추가하면 여러 사용자가 함께 쓸 수 있기도 하나 기본적으로는 단일 사용자 OS다.)
    - 다중 사용자 multi user
        - UNIX, NT server
        - 계정 여러개 만들어서 동시 접속 할 수 있다.
        - 사용자간 형평성: 자원관리
        - 다른 사람의 활동을 볼 수 없게 하는 보안
3. 처리 방식
    - 일괄 처리 batch processing
        - 작업이 있을 떄 바로 처리하지 않고 모았다가 한번에 처리한다.
        - ex) 키보드 두드렸을 때 한참 뒤에 결과가 출력
        - 일반적이진 않은 컴퓨터 시스템: 역사 속의 시스템
        - 효율성을 추구하기 위함.
    - 시분할 time sharing   
        - 현대 운영체제는 대부분 시분할 방식이다.
        - 작업은 동시에 실행되지만 운영체제가 작업을 번갈아가면서 CPU에 할당하는 시분할.
        - interactive하다: 컴퓨터 키보드를 눌렀을 때 바로 결과가 나오는 방식
        - 짧은 응답시간이 특징.
        - 데드라인이 있는건 아님: 사람이 느끼기에 빠르게 해주면서 주어진 자원을 최대한 활용하는 시스템이기 때문에 실행 시간을 보장하지는 않는다.
        - 범용 컴퓨터
    - 실시간 realtime os
        - **정해진 시간** 안에 결과가 나와야 하는 경우
        - 시분할과 비슷해보이나 완전 다르다
        - 원자로, 공장 제어, 미사일 제어, 반도체 장비 제어 ...
        - 특수한 목적을 가진 시스템
        - 파이프라이닝: 컴퓨터구조에서 배운다...?
            - 공정이 연관되어있어 
            - 반도체 공장에 정전이 났다: 지금까지 만들던거 다 폐기하고 처음부터 만들어야 하기 떄문에 약 한달동안 아무것도 만들지 못한다.
        - 분류
            - 데드라인 어기면 죽는거: hard realtime system, 경성 실시간
                - 반도체 공장장이 실직...
            - 데드라인 어겨도 안죽는거: soft realtime system, 연성 실시간
                - 기분이 나쁘지 뭔 일이 생기는건 아니다. 영화를 보면서 240p를 유지해야한다.
                - 사실 뭐... 영화볼 때 실시간 os를 쓰지는 않는다.
                - 하지만 데드라인을 필요로 하는 상황이 많이 생긴다: 내비게이션 (당장 우회전), 블랙박스 (사고 모두 기록해야함) 등

용어
multitasking

multiprogramming

time sharing

multiprocess

### reference
- [KOCW / 이화여자대학교 / 운영체제](http://www.kocw.net/home/enrolment/enrolmentView.do?cid=3646706b4347ef09&lid=af8e05c97c6d60de)