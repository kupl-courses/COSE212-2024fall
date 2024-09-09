# COSE212 - Programming Language, 2024 Fall
# 실습환경 안내: Local (Docker)

## HOW TO
### 1. Docker 설치
https://www.docker.com/

설치 확인: CLI에서 `docker --version` 실행 (버전은 달라도 됨)
```console
ta@cose212:~$ docker --version
Docker version 27.1.1, build 6312585
```

### 2. Visual Studio Code (VSC) 설치
https://code.visualstudio.com/

### 3. VSC Extension 'Dev Containers' 설치

### 4. Dev container 실행
1. Clone this repository
    ```console
    ta@cose212:~$ git clone https://github.com/kupl-courses/COSE212-2024fall.git
    ```
    (필요시 git 다운로드: https://git-scm.com/downloads)
2. Open in VSC
    ```console
    ta@cose212:~$ code COSE212-2024fall
    ```
3. 우측 아래 메시지의 'Reopen in Container' 클릭

    메시지가 뜨지 않을 경우 좌측 아래의 'Open a Remote Window' 버튼 클릭 후 'Reopen in Container' 클릭

## 코드 실행
### REPL 사용
VSC 터미널에서 `ocaml` 또는 `utop` 실행
```console
$ ocaml
```
또는
```console
$ utop
```
Tip) .ocamlinit 파일에 `#use "<파일명>.ml"`을 작성하면 REPL 실행시에 해당 파일을 자동으로 불러옴

### OCaml 스크립트 실행 (;;로 구분 필요)
VSC 터미널에서 `ocaml <파일명>.ml` 또는 `ocaml < <파일명>.ml` 실행
```console
$ ocaml < src/scratch_pad.ml
```

### .ml 파일 컴파일 및 실행 (;;로 구분 필요 없음)
VSC 터미널에서 `ocamlc -o <실행파일명> <파일명>.ml` 또는 `ocamlopt -o <실행파일명> <파일명>.ml` 이용
```console
$ ocamlopt -o main main.ml
$ ./main
```