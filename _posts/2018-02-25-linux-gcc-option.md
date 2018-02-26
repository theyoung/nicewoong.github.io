---
layout:     post
title:      "Linux GCC 옵션"
subtitle:   "Linux GCC Option" 
date:       2018-02-24 12:00:00
categories: [development]
author:     "nicewoong"
tags:       [development, linux, c, language, programming, c++]
comments: true
---


## gcc 옵션정리 

### gcc 전역 옵션 

* 옵션 
  * 설명 

* `-E `
  * 전처리 과정 화면에 출력 

* `-S `
  * 어셈블리 파일 생성 

* `-c` 
  * 오브젝트 파일 생성 

* `-v `
  * 컴파일 과정 화면에 출력 

* `--save-temps `
  * 컴파일시 생성되는 중간 파일 저장 

* `-da `
  * 컴파일 과정에서 생성되는 중간 코드 생성(RTL파일 등 생성) 


### 전처리기(cpp0)옵션 

옵션 
설명 

* `-l[패스] `
  * 헤더 파일을 탐색할 디렉토리 지정 ex_ -l/opt/include 

* `-include [헤더 파일 패스] `
  * 해당 헤더 파일을 모든 소스 내 추가 ex_ -include /root/my.h 

* `-D[매크로] `
  * 외부에서 #define 지정 ex_ -DDEBUG 

* `-D[매크로]=[매크로 값] `
  * 외부에서 해당 매크로를 정의하고 값을 지정 ex_ -DDEBUG=1 

* `-U[매크로] `
  * 외부에서 #undef 지정 ex_ -UDEBUG 

* `-M 또는 -MM `
  * make 기술파일을 위한 소스 파일의 종속 항목 출력 

* `-nostdinc `
  * 표준 C 헤더 파일을 include 하지 않음 

* `-C `
  * 전처리 과정에서 주석을 제거하지 않음 

* `-Wp,[옵션 리스트] `
  * 옵션 리스트를 전처리기에 바로 전달 






### C 컴파일러(cc1) 옵션 

#### - C언어 옵션 

옵션 
설명 

* `-ansi   `
  * ANSI C 문법으로 문법 검사 

* `-std=[C 표준] `
  * 지정한 C 표준으로 문법검사(표준:c89, c99, gnu89, gnu99 등) 

* `-traditional `
  * K&R C 문법으로 문법 검사 

* `-fno-asm `
  * asm, inline, typeof 키워드를 사용하지 않음 


#### - 경고옵션 

옵션 
설명 

* `-Wall -W` 
  * 모든 경고 메시지 출력 

* `-w `
  * 모든 경고 메시지 제거 

* `-Werror `
  * 모든 경고를 오류로 취급하여 컴파일 중단 

* `-pedantic `
  * C89 표준에서 요구하는 모든 경고 메시지를 표시 

* `-pedantic-error `
  * C89 표준에서 요구하는 모든 오류 메시지를 표시 

* `-Wtraditional` 
  * ANSI C와 K&R C 간에 서로 다른 결과를 가져올수 있는 부분이 있다면 경고 


#### 최적화 옵션 

옵션 
설명 

* `-O0 `
  * 아무런 최적화를 수행치 않음 

* `-O1` 또는` -O` 
  * 최적화 레벨 1수행 

* `-O2 `
  * 최적화 레벨 2 수행 

* `-O3` 
  * 최적화 레벨 3 수행 

* `-Os` 
  * 사이즈 최적화 수행 


- 디버깅 옵션 

옵션 
설명 

* `-g `
  * 바이너리 파일에 디버깅 정보 삽입 

* `-pg `
  * 프로파일을 위한 코드 삽입 


<br>
## 출처 
* (유닉스, 리눅스 프로그래밍) 필수 유틸리티 : vi, make, gcc, gdb, cvs, rpm 
