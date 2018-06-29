# hyunto-example/ansible

앤서블을 공부하고 연습하기 위한 GitHub Repository 입니다.

## 참고 문서/서적
* [앤서블 철저 입문](http://book.naver.com/bookdb/book_detail.nhn?bid=12685925)

## 사용법
### Requirements
* Python 2.7
* Vagrant
* Dockerpi
* Atom

### Ansible 설치

#### pip 버전 다운그레이드 (10.0.0 이하)

2018.06.29 현재 pip 10.0.0 이상 버전에서 ansible-container 설치시 `from pip.req import parse_requirements` 구문에서 `ImportError: No module named req` 에러가 발생하고 있습니다.

GitHub의 [관련 이슈](https://github.com/ansible/ansible-container/issues/945)를 보면 Bug Fix는 완료되었으나 최신 버전 릴리즈가 되지 않았기 때문에 아직 사용할 수 없습니다.

따라서 새로운 릴리즈가 있기 전까지 pip 9.x 이하 버전을 사용해야 합니다.
```bash
$ pip2 install 'pip<10.0.0'
$ pip2 -V
```

#### Virtual Environment 추가 및 활성화
```bash
$ pip2 install virtualenv
$ python2 -m virtualenv py27-ansible
$ cd py27-ansible
$ source bin/activate
```

#### 의존성 패키지 설치
```bash
$ pip install -r requirements.txt
```
