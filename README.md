# jenkins_practice

## 公式イメージ

https://github.com/jenkinsci/docker/blob/master/README.md


## jenkins起動

```bash
$ docker run -d \
    -v jenkins_home:/var/jenkins_home \
    -p 8080:8080 -p 50000:50000 \
    --name jenkins \
    jenkins/jenkins:lts
```

## 初回パスワード確認

```bash
# 最初のadminパスワード
$ docker exec -it jenkins bash
$ cat /var/jenkins_home/secrets/initialAdminPassword
XXXXXXXXXXXXXXXXXX
```
