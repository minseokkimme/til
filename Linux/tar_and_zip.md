## tar 명령어
### 사용법
- tar [기능] [아카이브 파일] [묶을 파일1] [묶을 파일2].....
### 태그
vf는 항상 붙습니다.

|태그 이름|기능|
|:-----:|:------:|
|-c|새로운 아카이브 파일을 생성|
|-x|아카이브 파일에서 여러 파일을 해제(압축 해제)|
|-t|아카이브 파일에서 안의 내용을 조회|
|-v|명령어 수행과정을 자세히 출력|
|-f|아카이브 장치 지정|



#### 아카이브 생성
![](https://images.velog.io/images/minseok0818/post/f42d2612-d3fc-4233-ac64-f3037e6c60bb/image.png)
#### 아카이브 해제
![](https://images.velog.io/images/minseok0818/post/d702392f-c30c-4ce9-b5ea-ceafe4b712f5/image.png)

### tar파일의 용량 문제
tar로 파일을 아카이브로 만들었을 때, 내용이 없는 파일을 압축하더라고 용량이 크게 나오는 것을 알 수 있다.
![](https://images.velog.io/images/minseok0818/post/d999fb8c-efc8-4e35-af85-01ef375a180f/image.png)
따라서 이 문제를 해결하기 위해서 tar로 압축된 파일을 gzip와 같은 압축하는 명령어로 다시 한번 압축해서 사용합니다.
## gzip, gunzip 명령어
### 사용법 
#### 압축
- gzip [압축 파일 이름]
![](https://images.velog.io/images/minseok0818/post/7d8a7736-0769-4720-abd1-359e44ddc297/image.png)
#### 압축 해제
- gunzip [압축 파일 이름]
![](https://images.velog.io/images/minseok0818/post/f968693c-f337-4982-8efe-07f0da16fe1f/image.png)
- tar.gz(tar로 압축하고 gzip로 압축되어 있는 경우)를 한번에 푸는 방법(tar 옵션에 z 추가)
![](https://images.velog.io/images/minseok0818/post/9e5491eb-f097-426a-a14e-9943dfaa1d92/image.png)

