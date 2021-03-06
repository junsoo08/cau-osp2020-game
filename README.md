# LOA 게임 프로젝트

- 2020년 2학기 중앙대학교 예술공학대학 오픈소스프로그래밍 수업의 과제입니다.
- 모든 공지는 슬랙(Slack) 채널을 통해 전달되고 있으니 수시로 슬랙을 확인하시기 바랍니다.
- [`participants.md`](participants.md) 에 참가자 본인의 계정 정보가 바르게 기록되어 있는지 확인하시고 이상이 있는 경우 슬랙 DM을 통해 알려주시기 바랍니다.

## 게임 진행 방법
- Python 개발 환경 구축 (강의 영상 참고).
- `loa`(https://github.com/daew0n/loa) 패키지 설치.
- `loa` 패키지에서 제공하는 클래스를 기반으로 자신만의 유닛(unit)과 팀(team) 클래스를 작성.
- 참가자가 정의한 팀 클래스는 `team.py` 모듈의 `get_team()` 함수를 통해 인스턴스화(instantiation)가 가능해야 함.
- `team.py` 모듈 파일을 `cau-osp2020` 개인저장소에 업로드.
    - `cau-osp2020`에 자동으로 생성되는 `student_xxxxxxxx` 디렉토리 내에 `team.py` 모듈 파일을 작성.
    - `team.py` 모듈은 `get_team()` 함수를 제공해야 하며, `get_team()` 함수의 역할은 `loa.Team`의 파생 클래스를 인스턴스화하여 리턴하는 것임.
    - `team.py` 모듈에서 별도 모듈을 활용하고자 하는 경우,
      별도 모듈 파일은 반드시 `student_xxxxxxxx` 디렉토리 내에 있어야 하며 `team.py`에서 해당 모듈을 **상대경로**로 불러들임(`import`).
- 서버에서 일정 시간 간격으로 모든 참가자의 `cau-osp2020` 개인저장소를 다운로드하며, `team.py`에 정의된 팀 객체를 이용하여 리그를 진행.
- 일정 시간 간격으로 리그 결과를 `leaderboard-round-xx.md`에 게시.

## 게임 규칙
- 라운드 별로 정의된 <strong>제한 규칙(constraints)</strong>에 따라 유닛 및 팀을 제작해야 함.
- 모든 참가자들이 서로 한번씩 대결함. 즉, 총 `n(n-1)/2`회의 대결을 진행.
- 두 참가자의 한 대결에서, `p` 횟수의 턴(turn)으로 구성된 단위 대결을 `q` 횟수만큼 반복하여 최종 승패를 결정함. 예를 들어, 단위 대결은 `20`회의 턴으로 구성되며, 단위 대결을 `10`회 반복하여 더 많이 이긴 참가자가 최종 승리하게 됨.
- 두 참가자가 대결한 결과, 승리한 참가자는 승점 **3점**을 획득하며 패한 참가자는 승점이 없음.
- 두 참가자가 비긴 경우 두 참가자 모두 승점 **1점**을 획득.
- 각 라운드 마감 시점에서 최종 순위 및 승점을 해당 라운드의 최종 점수로 함.
- 특정 라운드에서 마감일 이전에 달성한 순위 및 승점은 누적되지 않음.
- 각 라운드에서 획득한 점수를 합하여 이 프로젝트의 최종 점수를 결정.
- 각 라운드 종료 이후 상위권 참가자의 코드를 모두 공개
- 코드에 문제가 있는 경우 퇴장 처리.
   - 제출한 코드에서 `print()`를 사용할 수 없음.

## 라운드 최종 점수 계산
  획득한 승점 *X*에 대해 아래 수식에 근거하여 변환 계수 a와 b를 구하고, a*X* + b를 최종 점수(final score)로 한다.
  - a*Xmax* + b = 100.
  - a*Xmean* + b = 80.


## 라운드 및 제한 규칙 정의
- 제 1 라운드
    - 마감일: 12월 11일 금요일 11:59 PM
    - 규칙: [constraints-round-01](constraints/constraints-round-01.ipynb)
    - 명예의전당: [hall-of-fame/round-01](hall-of-fame/round-01)
    - 최종 점수: [finalscore-round-01](finalscore-round-01.md)
- 제 2 라운드
    - 마감일: 12월 15일 화요일 23:59 PM
    - 규칙: [constraints-round-02](constraints/constraints-round-02.ipynb)
    - 명예의전당: [hall-of-fame/round-02](hall-of-fame/round-02)
    - 최종 점수: [finalscore-round-02](finalscore-round-02.md)
- 제 3 라운드
    - 마감일: 12월 18일 금요일 23:59 PM
    - 규칙: [constraints-round-03](constraints/constraints-round-03.ipynb)   
- 제 4 라운드
    - 마감일: 12월 17일 목요일 12:00 PM
    - 규칙: *추후 공지*    
