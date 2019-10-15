# Programming Languages course @ HNU CE grad school
2019년 2학기 한남대학교 컴퓨터공학과 대학원 **프로그래밍언어**(의미론) 과목 홈페이지입니다.
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/hnu-pl/grad-pl2019fall/master?urlpath=lab)
[![NBviewer](./nbviewer_badge.svg)](https://nbviewer.jupyter.org/github/hnu-pl/grad-pl2019fall/tree/master/)


###### Weekly class schedule:
| day |   time      | room#  |
|-----|-------------|--------|
| Tue | 19:00-21:50 | 90327  |

<!-- [Hi-Class 과목 페이지로 바로가기](https://hiclass.hannam.ac.kr/courses/9273) -->

## Textbook
* 주교재
    - [Practical Foundations for Programming Languages (2nd ed.)](https://www.cs.cmu.edu/~rwh/pfpl/) by Rober Harper, Cambridge University Press, 2016
* 부교재
    - [Programming in Haskell (2nd ed.)](http://www.cs.nott.ac.uk/~pszgmh/pih.html) by Graham Hutton, Cambridge University Press, 2016
* 참고도서
    - [Types and Programming Languages](https://www.cis.upenn.edu/~bcpierce/tapl/) by Benjamin C. Pirce, The MIT Press, 2002
    - [Homotopy Type Theory](https://homotopytypetheory.org/book/) by the Univalent Foundations Program
    - [Programming Language Foundations in Agda](https://plfa.github.io/)

## Course topics and memo

##### 0903 untyped lambda calculus
 * call-by-value, call-by-name, call-by-need
     - OCaml은 call-by-value이고 Haskell은 call-by-need인데 차이점을 보여주는 예제
         * https://try.ocamlpro.com/ 에서 `let rec loop()=loop() in (fun x -> 3) (loop())` 실행해 보라
         * https://tryhaskell.org/ 에서 `let loop()=loop() in (\x -> 3) (loop())` 실행해 보라
 * https://crypto.stanford.edu/~blynn/lambda/
 * Church encodings (boolean, natural numbers)
     - 기본 상수(constant)를 추가하지 않고 람다식으로 구성된 함수만으로 계산이 가능함을 보여준다
 * 참고도서 TAPL (Part I - Chapter 5)

##### 0910 simply-typed lambda calculus
 * 단순타입 람다계산법은 람다식이 함수 타입인지 함수가 아닌 기본 타입인지 등을 구분할 수 있는 타입 시스템이 추가됨
 * https://crypto.stanford.edu/~blynn/lambda/simply.html
     - 위 URL에 나타난 것은 함수정의식에 `(\x:t.e)`와 같이 인자 변수의 타입 표기가 추가된 Church 스타일의 STLC이다
     - 이에 대비되는 Curry 스타일의 STLC도 있는데 함수정의식이 `(\x.e)`로 타입없는 람다계산법과 같다
 * 참고도서 TAPL (Part II - Chapter 9)

##### 0917 recursion and recursive types, System F, System Fω
 * fixpoints in untyped lambda calculus 
 * 참고도서 TAPL (Part V)
 * 참고도서 TAPL (Part VI)

##### 0924 
 * call-by-value, call-by-need: hsnote 디렉토리 노트북 파일들
 * Curry-Howard correspondence의 개념과 간단한 예
 * 타입 보존 정리 및 조심하지 않으면 실제 프로그래밍 언어에서 잘 성립되지 않을 수 있는 사례들 

##### 1001
타입 보존 정리 관련해서 구체적인 예
 * Scala에서 covariant, contravariant 제너릭 인자
   https://www.journaldev.com/9585/scala-variances-covariant-invariant-contravariant
 * ML계열 언어에서 value restriction으로 polymorphism 제한
참고도서 PLFA 실습

#### 1008
* DSL for the Uninitiated라는 ACM Comm. 기사
* eDSL에 활용되기도 하는 HOAS

#### 1015
* 패턴매칭과 일치화
* 타입 유추 과정에서 만들어지는 일치화 방정식을 Prolog를 이용해 자동으로 풀이 
* Prolog의 특징과 타입 규칙을 Prolog로 만들어 보기

