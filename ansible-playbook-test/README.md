# Playbook Test

## Reference
* [Testing Strategies](https://docs.ansible.com/ansible/latest/reference_appendices/test_strategies.html)

## ansible-playbook Test Options
* --syntax-check : Perform a syntac check on th playbook, but do not execute it.
* --check : Don't make any changes; instead, try to predict some of the changes that may occur

```bash
$ ansible-playbook --syntax-check check_mod.yml
$ ansible-playbook --check check_mod.yml
```

## Useful modules for testing
* wait_for : 특정 포트가 실행되고 있는지, 지정한 경로에 파일이 있는지와 같은 조건을 정의하고, Sleep 명령과 같이 일정 시간, 조건이 맞을 때까지 기다린다.

* uri : register, fail, when을 조합하여 지정한 URL에서 콘텐츠를 얻고, 출력된 결과에 특정 문자열이 포함되어 있지 않을 때 태스크를 정지합니다.

* assert : that 파라미터에서 정의한 조건에 맞는지 판단하고 일치하지 않으면 태스크를 실패시킵니다.
