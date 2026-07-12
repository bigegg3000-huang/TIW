# vim
vim은 리눅스 패키지 중 하난데 문서 편집기다.

<img width="800" height="565" alt="image" src="https://github.com/user-attachments/assets/e66f94b0-89ca-4600-96aa-106e0f20c042" />

모드가 4개 있으며 이거 번갈아가면서 하면 된다.

<img width="1082" height="847" alt="image" src="https://github.com/user-attachments/assets/384bfdc5-11af-4b02-b7ef-34844d05b03a" />


## 시작과 종료
시작은
```bash
vim
```
혹은 원하는 파일을 vim으로 열려면
```bash
vim thisiscode.py
```

종료는 Normal Mode(Esc)에서는
```
ZZ : 저장하고 종료
ZQ : 저장하지 않고 종료
```

Command-Line Mode(:)에서는
```
:wq : 저장하고 종료
:q! : 저장하지 않고 종료
```


## Normal Mode
기본적으로 시작하거나 esc를 눌러 나오는 모드인 Normal Mode가 있다.
Normal mode는 커서 이동, 삭제, 복사, 복붙은 되는데 입력은 안 된다.

커서이동을 그냥 화살표키나 마우스로 클릭해도 되긴 되는데 명령어로 해도 된다.
```
# 글자 이동
h  : 왼쪽으로 한 칸
j  : 아래로 한 줄
k  : 위로 한 줄
l  : 오른쪽으로 한 칸

w  : 다음 단어의 시작으로
b  : 이전 단어의 시작으로
e  : 현재 단어의 끝으로

0  : 줄의 맨 앞으로
$  : 줄의 맨 뒤로
H = gg : 문서의 맨 처음으로
M : 문서의 중간으로
L = G  : 문서의 맨 끝으로
nG : 문서의 n번째 줄로
```

텍스트 편집도 있다.
```
# 복사
yy  : 한줄 복사
yyn : n줄 만큼 복사 (똑같은걸 n줄 복사)  
yw  : 한 단어 복사 (yank word) 
ynw : n 단어 복사 (똑같은 단어를 n번 복사) 
y$  : 커서부터 이줄 끝까지 복사 
y0  : 커서부터 이줄 앞까지 복사 메

# 붙여넣기 
p : 커서 앞으로 붙여넣기
P : 커서 뒤로 붙여넣기 

# 삭제
x : 커서 뒤의 문자 하나 삭제
X : 커서 앞에 문자 하나 삭제 
dd : 한줄 삭제
ddn : n줄 삭제 
dw : 한 단어 삭제 (delete word) 
dnw : n 단어 삭제 
d$ : 커서부터 이줄 끝까지 삭제
d0 : 커서부터 이줄 앞까지 삭제 
dG : 커서부터 문서 끝까지 삭제  
```

검색이나 치환, 기타 기능들도 있다.
```
# 검색
/nn : 순방향으로 nn 문자열 검색
?nn: 역방향으로 nn 문자열 검색

# 치환
%s/nn/mm : nn을 mm으로 문자열 치

# 언도우, 리도우
u : 실행 취소
Ctrl+r : 되돌리기

# 기타
. : 마지막 명령 반
```

## Insert Mode
글자 입력하면 된다.
i, a를 누르면 Insert Mode가 되며 글 넣을 수 있다. 이외에도 I, A, o, O, s, S를 눌러도 전환이 가능하다.

## Command Mode
파일 저장같은거 하는 모드다.
```
:w          : 저장
:q          : 종료
:wq 또는 :x -:저장하고 종료
:q!         : 저장하지 않고 강제 종료

:e 파일명   : 파일 열기
:w 파일명   : 다른 이름으로 저장

:set number : 줄 번호 표시
:help       : 도움말
```

## Visual Mode
글자 선택하는데 사용하는 모드다.

글자를 선택해서 뭔가 들여쓰기를 한다던지, 대소문자로 변경한다던지 그런 걸 한다.
