# git basic command

## 버전 관리란?
 버전 관리 시스템은 파일 변화를 시간에 따라 기록했다가 나중에 특정 시점의 버전을 다시 꺼내올 수 있는 시스템이다. 

---

## 분산 버전 관리 시스템(DVCS)

### github에서 사용

![DVCS](./assets/distributed.png)

## 3가지 상태

![areas](./assets/areas.png)


---
## 명령어

```shell 
git init

```
- `.git directory`를 생성하는 명령어

```shell
git add .
```
- `working directory`에 있는 파일, 폴더를 `staging area`에 추가
- 무대에 오르기
- add 하기 전에 파일이 저장되었는지 확인하기

```shell
git commit -m 'message'
```
- `staging area`에 올라간 파일들을 저장
- 무대에 올라간 사진 찍기

```shell
git remote add origin <remoteurl>
```
- 원격저장소 주소를 `origin`이라는 별명으로 저장
- 최초 한 번만 시행 (컴퓨터 재실행 시에 시행 X)

```shell
git push origin master
```
- `master` 브런치를 `origin` 원격저장소로 업로드
- 사진을 github과 연결해서 업로드

