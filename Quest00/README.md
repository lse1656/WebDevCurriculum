# Quest 00. 형상관리 시스템

## Introduction
* git은 2021년 현재 개발 생태계에서 가장 각광받고 있는 버전 관리 시스템입니다. 이번 퀘스트를 통해 git의 기초적인 사용법을 알아볼 예정입니다.

## Topics
* git
  * `git clone`, `git add`, `git commit`, `git push`, `git pull`, `git branch`, `git stash` 명령
  * `.git` 폴더
* GitHub

## Resources
* [Resources to learn Git](https://try.github.io)
* [Learn Git Branching](https://learngitbranching.js.org/?locale=ko)
* [Inside Git: .Git directory](https://githowto.com/git_internals_git_directory)

## Checklist
* 형상관리 시스템은 왜 나오게 되었을까요?<br/>
&nbsp;개발을 하다 보면 잘못 만들어진 소스코드를 되돌릴 필요도 있고 변경된 이력도 확인해야하며 특히 여러명의 개발자가 협업할 때 발생하는 충돌을 처리하기 위해 형상관리 시스템이 필요하다. 
<br/><br/>
* git은 어떤 형상관리 시스템이고 어떤 특징을 가지고 있을까요? 분산형 형상관리 시스템이란 무엇일까요?<br/>
&nbsp; git은 버전 관리 시스템(Version Control System, VCS)으로 <strong>분산형 형상관리(Distributed VCS) 시스템</strong>에 속한다. 개발자가 중앙 서버에 접속하지 않은 상태에서도 코딩 작업을 진행할 수 있도로 지원해준다. 특징으로는 팀 개발을 위한 분산 환경 코딩에 최적화 되어 있고 로컬에 다수의 독립성이 보장되는 branch를 허용하고 쉽게 생성,삭제,병합이 가능하다는 점이 있다.<br/>
&nbsp;버전 관리 시스템은 크게 두가지로 분류할 수 있는데 첫째는 중장집중형 버전관리이고 둘째는 분산형 버전관리이다. 중앙집중형은 중앙 서버에 올라간 소스코드를 사용자가 내려받아 작업하고, 작업이 완료된 결과물을 commit하여 서버로 올려보내는 방식이다. commit한 내용이 바로 중앙 서버로 업로드 되는 방식이므로 그 소스를 공유하는 모든 작업자에게 영향이 간다. 대표적인 시스템으로 SVN이 있다. 분산형은 작업 히스토리를 각자의 서버에 저장해 관리될 수 있어 같은 파일 하나를 여러명이 동시에 작업하는 병렬 개발이 가능하고 개인작업과 공동작업을 분리할 수 있기에 충돌을 최소화 시켜준다.
  * git은 어떻게 개발되게 되었을까요? git이 분산형 시스템을 채택한 이유는 무엇일까요?
  <br/><br/>
* git과 GitHub은 어떻게 다를까요?
&nbsp; git은 버전관리를 위한 툴이고, Github는 git으로 저장되어 원격전송된 내역들이 저장되는 공간을 제공해주는 서비스이다.
<br/><br/>
* git의 clone/add/commit/push/pull/branch/stash 명령은 무엇이며 어떨 때 이용하나요? 그리고 어떻게 사용하나요?<br/>
&nbsp; git clone - 기존 소스 코드를 다운로드 및 복제한다. 즉, 원격 저장소의 프로젝트를 로컬에서 이용할 수 있도록 복사해준다.<br/>
&nbsp; git add - 수정한 파일들을 stage area에 올려주어 commit 가능한 상태로 만들어준다.<br/>
&nbsp; git commit - staged된 변경사항들의 변경을 확정짓고 기록을 남긴다.<br/>
&nbsp; git push - 로컬 저장소에 남긴 기록들을 원격 저장소(remote 저장소)에 적용시킨다.<br/>
&nbsp; git pull - push와 반대로 원격 저장소에 있던 프로젝트의 변경사항을 로컬저장소로 가져온다. 변경사항을 가져옴과 동시에 병합 시키기 때문에 무엇이 추가 되었고 병합 되었는지 확인 불가.<br/>
&nbsp; git branch - 작업물이 분기된다.<br/>
&nbsp; git stash - 아직 마무리하지 않은 작업물을 스택에 잠시 저장시킨다. 이를 통해 아직 완료되지 않은 일을 commit하지 않고 나중에 다시 꺼내와 마무리 할 수 있다.
<br/><br/>
* git의 Object, Commit, Head, Branch, Tag는 어떤 개념일까요? git 시스템은 프로젝트의 히스토리를 어떻게 저장할까요?
<br/><br/>
* 리모트 git 저장소에 원하지 않는 파일이 올라갔을 때 이를 되돌리려면 어떻게 해야 할까요?<br/>
파일을 되돌리는 방식은 크게 두가지가 있는데 첫째는git reset 을 이용하여 커밋을 취소하는 방식이고 둘째는 git revert을 사용하여 커밋 내용을 되돌리는 방식으로 기록이 남게된다.

## Quest
* GitHub에 가입한 뒤, [이 커리큘럼의 GitHub 저장소](https://github.com/KnowRe-Dev/WebDevCurriculum)의 우상단의 Fork 버튼을 눌러 자신의 저장소에 복사해 둡니다.
* Windows의 경우 같이 설치된 git shell을, MacOSX의 경우 터미널을 실행시켜 커맨드라인에 들어간 뒤, 명령어를 이용하여 복사한 저장소를 clone합니다.
  * 앞으로의 git 작업은 되도록 커맨드라인을 통해 하는 것을 권장합니다.
* 이 문서가 있는 폴더 바로 밑에 있는 sandbox 폴더에 파일을 추가한 후 커밋해 보기도 하고, 파일을 삭제해 보기도 하고, 수정해 보기도 하면서 각각의 단계에서 커밋했을 때 어떤 것들이 저장되는지를 확인합니다.
* `clone`/`add`/`commit`/`push`/`pull`/`branch`/`stash` 명령을 충분히 익혔다고 생각되면, 자신의 저장소에 이력을 push합니다.

## Advanced
* Mercurial은 어떤 형상관리 시스템일까요? 어떤 장점이 있을까요?
* 실리콘밸리의 테크 대기업들은 어떤 형상관리 시스템을 쓰고 있을까요?
