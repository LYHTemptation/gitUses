## 분산버전관리시스템(DVCS)

> **중앙집중식버전관리시스템**은 중앙에서 버전을 관리하고 파일을 받아서 사용
>
> **분산버전관리시스템**은 원격 저장소(remote repository)를 통하여 협업하고, 모든 히스토리를 클라이언트들이 공유

### 원격저장소 설정 명령어

* remote 확인

  ```bash
  $ git remote -v
  ```

* remote 추가

  ```bash
  $ git remote add <이름> <url>
  ```

* remote 삭제

  ```bash
  $ git remote rm <이름>
  ```

* remote url 변경

  ```bash
  $ git remote set-url <이름> <url>
  ```

* remote  이름 변경

  ```bash
  $ git remote rename <이름> <url>
  ```

***

### 원격저장소 활용 명령어

```bash
# 원격 저장소를 복제하여 가져옴
$ git clone <원격저장소주소>
```

```bash
# 원격 저장소로 로컬 저장소 변경 사항(커밋)을 올림(push)
# 로컬 폴더의 파일/폴더가 아닌 저장소의 버전(커밋)이 올라감
$ git push <원격저장소이름> <브랜치이름>
```

```bash
# 원격 저장소로부터 변경된 내역을 받아와서 이력을 병합함
$ git pull <원격저장소이름> <브랜치이름>
```



***

### 원격저장소 순서

1. 로컬에 폴더 생성

2. ```bash
   # 폴더 위치로 이동 후 git 저장소 생성
   $ git init
   ```

3. ```bash
   # git 파일 add
   $ git add <file>
   ```

4. ```bash
   # git commit
   $ git commit # 메시지 편집 창(기본 Vim)
   $ git commit -m '메시지'
   ```

5. github에 원격저장소(repository) 생성

6. ```bash
   # 원격저장소 등록
   $ git remote add origin https://github.com/username/repository_name.git
   ```

7.  ```bash
    # 파일/폴더 push
    $ git push origin master
    ```

   

