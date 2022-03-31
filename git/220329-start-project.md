## git 설치 후 user.name,user.email 초기 설정

1. git config —global [user.name](http://user.name) =”user.name”
2. git config —global [user.email](http://user.email) = “user.email”

([user.name](http://user.name) 설정을 잘 못 했을 경우 → git config —unset user.name or user.email)

(user.name이 중복된 값이 있을 경우 → git config --unset-all --global user.name)

설정 잘 됐는지 확인

 → git config —list

## CLI (Command Line Interface) -명령어

- ls : 해당 directory에 있는 파일들을 보여준다.
    - ls -a : 숨김파일도 보여준다.
    
- touch : 해당 directory에 파일을 만들어준다.
    - touch 생성할파일이름 (ex, touch file.txt) - 확장자까지 표시
    
- mkdir : 새로운 directory를 생성한다.
    - mkdir 생성할 directory 이름 (ex, mkdir dir1)
    
- cd : 해당 directory에 접근하기 위한 명령어
    - cd dir1/ - dir1으로 이동
    - cd .. - 상위 directory로 이동 ( .. : 상위 directory , . : 현재 directory)
    
- rm : 파일을 삭제하기 위한 명령어
    - rm 파일이름 (ex, rm file)
    - *(에스터리스트)를 이용한 파일 삭제
        - file.txt file1.txt file2.txt → 모든 파일을 삭제하기 위해서 *을 사용한다
        
        ex) rm *.txt → 확장자 txt를 가진 파일들을 모두 삭제한다.
        
    
- cp : 파일을 복사하기 위한 명령어
    - cp (해당파일이름) (바꿀파일이름) (ex, cp file file1)
        
        해당 directory에 있는 file을 file1이름으로 복사
        
    - cp (해당파일이름) (directory이름) (ex, cp file dir1/)
        
        해당 directory에 있는 file을 dir1이라는 directory에 복사
        
- mv : 파일을 이동하기 위한 명령어
    - mv (파일이름) (이동할 directory 이름) (ex, mv file dir1/)
        
        해당 directory에 있는 file을 dir1로 이동

## git clone
- git clone [clone할 주소] (선택사항 : 파일 위치 설정)

## git init
