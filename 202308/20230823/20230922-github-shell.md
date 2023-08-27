# 1

~/Downloads/hobbyloop/hobbyloop-be   dongmoo/update >R>  
`git remote update`

- 결과
```shell
  remote: Enumerating objects: 1, done.
  remote: Counting objects: 100% (1/1), done.
  remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
  Unpacking objects: 100% (1/1), 750 bytes | 375.00 KiB/s, done.
  From https://github.com/hobbyloop/hobbyloop-be
  7ee544b..f0c3566  develop       -> origin/develop
* [new branch]      release/0.0.1 -> origin/release/0.0.1
```
---
# 2

~/Downloads/hobbyloop/hobbyloop-be   dongmoo/update >R>  
`git remote prune origin`

- 결과
```shell
  Pruning origin
  URL: https://github.com/hobbyloop/hobbyloop-be.git
* [pruned] origin/dongmoo/change-request-param-strategy
* [pruned] origin/dongmoo/cloudwatch
* [pruned] origin/dongmoo/conflict-solve
* [pruned] origin/dongmoo/exception-handler
* [pruned] origin/dongmoo/fix-deploy-bug
* [pruned] origin/dongmoo/lesson-info
* [pruned] origin/dongmoo/logging
* [pruned] origin/dongmoo/login-debug
* [pruned] origin/dongmoo/mypage-tickets
* [pruned] origin/dongmoo/querydsl-setting
* [pruned] origin/dongmoo/refactor-sevice-flow
* [pruned] origin/dongmoo/set-default-type
* [pruned] origin/dongmoo/swagger-paging
* [pruned] origin/dongmoo/ticket
* [pruned] origin/dongmoo/ticket-price-policy
* [pruned] origin/dongmoo/ticket-with-distance
* [pruned] origin/dongmoo/update-swagger-config
* [pruned] origin/dongmoo/userprofile-mypage
* [pruned] origin/dongmoo/userprofileinfo
* [pruned] origin/jeongmin/github-action-health-checker
* [pruned] origin/main
* [pruned] origin/road3144/updateSpringBootVersion
* [pruned] origin/xonmin/cloud-watch
```
---
# 3

~/Downloads/hobbyloop/hobbyloop-be   dongmoo/update >R>  
`git checkout develop`

- 결과
```shell
  Switched to branch 'develop'
  Your branch is behind 'origin/develop' by 4 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)
```
---

# 4

~/Downloads/hobbyloop/hobbyloop-be   dongmoo/update >R> 
`git checkout develop`

- 결과
```shell
  Switched to branch 'develop'
  Your branch is behind 'origin/develop' by 4 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)
```
---

# 5

~/Downloads/hobbyloop/hobbyloop-be   develop >R>  
`git pull origin develop`

- 결과
```shell
From https://github.com/hobbyloop/hobbyloop-be
* branch            develop    -> FETCH_HEAD
  Updating 7ee544b..f0c3566
  Fast-forward
  hobbyloop-api/src/main/java/hobbyloop/backend/api/applicationservice/center/CenterApplicationService.java    |  46 +++++++-------------
  .../src/main/java/hobbyloop/backend/api/applicationservice/facility/FacilityApplicationService.java          |  24 +++++++++++
  .../src/main/java/hobbyloop/backend/api/applicationservice/instructor/InstructorApplicationService.java      |  12 +++---
  hobbyloop-api/src/main/java/hobbyloop/backend/api/applicationservice/ticket/TicketApplicationService.java    |  16 +++----
  hobbyloop-api/src/main/java/hobbyloop/backend/api/controller/center/CenterController.java                    |  64 ----------------------------
  hobbyloop-api/src/main/java/hobbyloop/backend/api/controller/facility/FacilityController.java                |  62 +++++++++++++++++++++++++++
  .../api/controller/{center/dto/CenterListResponseDTO.java => facility/dto/FacilityInfoResponseDTO.java}      |  32 +++++++-------
  .../api/controller/{center/dto/CenterRankingListRequestDTO.java => facility/dto/FacilityListRequestDTO.java} |  10 ++++-
  hobbyloop-api/src/main/java/hobbyloop/backend/api/controller/ticket/dto/CreateTicketRequestDTO.java          |   2 +
  hobbyloop-api/src/main/java/hobbyloop/backend/api/controller/userprofile/dto/UserTicketInfoDTO.java          |   6 +--
  hobbyloop-domain/src/main/generated/hobbyloop/backend/domain/QDayTime.java                                   |  57 +++++++++++++++++++++++++
  hobbyloop-domain/src/main/generated/hobbyloop/backend/domain/center/QCenter.java                             |   6 ---
  hobbyloop-domain/src/main/generated/hobbyloop/backend/domain/facility/QFacility.java                         |  85 +++++++++++++++++++++++++++++++++++++
  hobbyloop-domain/src/main/generated/hobbyloop/backend/domain/instructor/QInstructor.java                     |   6 +--
  hobbyloop-domain/src/main/generated/hobbyloop/backend/domain/ticket/QTicket.java                             |   6 +--
  hobbyloop-domain/src/main/java/hobbyloop/backend/domain/center/Center.java                                   |  16 +------
  hobbyloop-domain/src/main/java/hobbyloop/backend/domain/center/CenterRepository.java                         | 127 ++++++++++++++++++++++++++-----------------------------
  hobbyloop-domain/src/main/java/hobbyloop/backend/domain/center/CenterService.java                            |  38 +----------------
  hobbyloop-domain/src/main/java/hobbyloop/backend/domain/center/{CenterDTO.java => FacilityDTO.java}          |  15 ++++---
  hobbyloop-domain/src/main/java/hobbyloop/backend/domain/facility/FacilityRepository.java                     |   6 +++
  hobbyloop-domain/src/main/java/hobbyloop/backend/domain/facility/FacilityService.java                        |  61 ++++++++++++++++++++++++++
  hobbyloop-domain/src/main/java/hobbyloop/backend/domain/instructor/Instructor.java                           |  11 +++--
  hobbyloop-domain/src/main/java/hobbyloop/backend/domain/instructor/InstructorRepository.java                 |   4 +-
  hobbyloop-domain/src/main/java/hobbyloop/backend/domain/instructor/InstructorService.java                    |   6 +--
  hobbyloop-domain/src/main/java/hobbyloop/backend/domain/ticket/Ticket.java                                   |   9 ++--
  hobbyloop-domain/src/main/java/hobbyloop/backend/domain/ticket/TicketRepository.java                         |   4 +-
  hobbyloop-domain/src/main/java/hobbyloop/backend/domain/ticket/TicketService.java                            |  14 +++---
  hobbyloop-domain/src/main/java/hobbyloop/backend/domain/ticket/UserTicketService.java                        |   8 ++--
  28 files changed, 460 insertions(+), 293 deletions(-)
  create mode 100644 hobbyloop-api/src/main/java/hobbyloop/backend/api/applicationservice/facility/FacilityApplicationService.java
  create mode 100644 hobbyloop-api/src/main/java/hobbyloop/backend/api/controller/facility/FacilityController.java
  rename hobbyloop-api/src/main/java/hobbyloop/backend/api/controller/{center/dto/CenterListResponseDTO.java => facility/dto/FacilityInfoResponseDTO.java} (55%)
  rename hobbyloop-api/src/main/java/hobbyloop/backend/api/controller/{center/dto/CenterRankingListRequestDTO.java => facility/dto/FacilityListRequestDTO.java} (61%)
  create mode 100644 hobbyloop-domain/src/main/generated/hobbyloop/backend/domain/QDayTime.java
  create mode 100644 hobbyloop-domain/src/main/generated/hobbyloop/backend/domain/facility/QFacility.java
  rename hobbyloop-domain/src/main/java/hobbyloop/backend/domain/center/{CenterDTO.java => FacilityDTO.java} (53%)
  create mode 100644 hobbyloop-domain/src/main/java/hobbyloop/backend/domain/facility/FacilityRepository.java
  create mode 100644 hobbyloop-domain/src/main/java/hobbyloop/backend/domain/facility/FacilityService.java

```
---

# 6

~/Downloads/hobbyloop/hobbyloop-be   develop >R> 
`git checkout dongmoo/update`

- 결과
```shell
  Switched to branch 'dongmoo/update'
```
---

# 7

~/Downloads/hobbyloop/hobbyloop-be   dongmoo/update >R> 
`git rebase develop`

- 결과
```shell
  fatal: It seems that there is already a rebase-merge directory, and
I wonder if you are in the middle of another rebase.  If that is the
case, please try
git rebase (--continue | --abort | --skip)
If that is not the case, please
rm -fr ".git/rebase-merge"
and run me again.  I am stopping in case you still have something
valuable there.
```
---

# 8

✘  ~/Downloads/hobbyloop/hobbyloop-be   dongmoo/update >R>  
`git rebase --continue`

- 결과
```shell
  Switched to branch 'dongmoo/update'
```
