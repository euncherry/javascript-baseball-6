# 구현할 기능 목록
>**숫자야구**
> >user가 컴퓨터가 선택한 1-9까지의 서로 다른 수로 이루어진 3자리의 수를 맞추는 게임</br>

</br>
</br>

### **게임 시작 문구 출력**
  ```
  숫자 야구 게임을 시작합니다.
  ```

## 게임 진행
> user에게 잘못된 값을 입력받을 경우 error처리후 종료.
### computer가 정답을 설정
- 컴퓨터가 1-9사이의 서로 다른 임의의 수 3개를 선택.
- 정답을 컴퓨터가 선택한 수로 초기화.

### user가 수를 입력함
- [x] **user에게 서로다른 3자리 수를 입력받음** 
	- 예시 : '123' , '145' , '671' ...
- [x] **`예외사항 처리` 서로 다른 3자리 수인지 확인**
	1. user의 입력이 1-9사이의 3개의 숫자로만 이루어져있지 않은 경우 `throw`를 통해 App종료
	2. user의 입력이 중복인 숫자가 있는 경우 `throw`를 통해 App종료

### user가 정답을 입력하지 못한 경우
- [x] **user가 입력한 수와 정답을 비교한 결과를 볼, 스트라이크 개수로 출력함**
  ```      
  1볼 1스트라이크
  ```
  - 스트라이크 : 같은 수가 같은 자리에 있음
  - 볼 : 숫자가 정답에 존재하고 다른 자리에 있음
  - 낫싱 : 정답과 같은수가 없음
	  
- [x] **user는 힌트를 이용해서 정답을 맞출 때 까지 다시 수를 입력함**

### user가 정답을 입력한 경우
> 3개의 숫자를 모두 맞힐 경우의 문구를 출력.</br>
> user에게 1혹은 2를 입력받아 게임을 다시 시작하거나 완전히 종료 가능.
- [x] **문구 출력**
  ```
  3스트라이크
  3개의 숫자를 모두 맞히셨습니다! 게임 종료
  ```
- [x] **user에게 수를 입력받음**
	- user에게 1을 입력 받은 경우 : 새로운 정답으로 게임진행 다시시작
	- user에게 2를 입력 받은 경우 : App종료
- [x] **`예외사항 처리` user가 입력한 값이 1 혹은 2 인지 확인**
	- user의 입력이 1 혹은 2가 아닌경우 `throw`를 통해 App종료