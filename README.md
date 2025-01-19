# Домашнее задание к занятию "`GitLab`" - `Арбузов Михаил`


### Задание 1

1. `Разверните GitLab локально, используя Vagrantfile и инструкцию, описанные в этом репозитории.`
2. `Создайте новый проект и пустой репозиторий в нём.`
3. `Зарегистрируйте gitlab-runner для этого проекта и запустите его в режиме Docker. Раннер можно регистрировать и запускать на той же виртуальной машине, на которой запущен GitLab.`


В качестве ответа в репозиторий шаблона с решением добавьте скриншоты с настройками раннера в проекте.

![Screenshot from 2025-01-20 00-09-14](https://github.com/user-attachments/assets/5fc5dbdb-6044-4127-86e2-d8c143dfdfb7)


---


### Задание 2

1. `Запушьте репозиторий на GitLab, изменив origin. Это изучалось на занятии по Git.`
2. `Создайте .gitlab-ci.yml, описав в нём все необходимые, на ваш взгляд, этапы`


В качестве ответа в шаблон с решением добавьте:

    файл gitlab-ci.yml для своего проекта или вставьте код в соответствующее поле в шаблоне;
    скриншоты с успешно собранными сборками.
```
.gitlab-ci.yml: 
stages:
  - test
  - build

test:
  stage: test
  image: golang:1.17
  script: 
   - go test .

build:
  stage: build
  image: docker:latest
  script:
   - docker build .

```

![Screenshot from 2025-01-20 00-23-46](https://github.com/user-attachments/assets/6b96d19d-32b2-4ca9-bd1a-e594eee79cba)


---


