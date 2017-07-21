在Docker Hub建立Automated Build Repository
=========================================
    freak@funP.com
    2017-07-21

---

**官方文件**

https://docs.docker.com/docker-hub/builds/

---

**為什麼想使用 Docker Hub?**
* 沒資源自己架 docker registry
* 自己架了還要 maintain & upgrade

**缺點:**
* lock-in
* 不付費的話只有一個 private repo

---

**為什麼想使用 Docker Hub?**
* 策略性的 Open 

---

```
$ docker build -t namespace/repo:tag ./
$ docker push
```

---

**為什麼 Automated Build**
* 提高使用者對你的 repository 的信任
* ~~找個刷github牆的理由~~

---

**在Docker Hub上進行Automated Build的需求**
* 註冊一個Docker Hub Account
* Dockerfile host 在 GitHub 或 Bitbucket 上的 git repository

---

**Demo一下過程**
* 將 Docker Hub Account 連結 GitHub
* 建立一個 Automated Build Repository
* 設定 Build Settingss
* commit to trigger a build
* 看一下 Build Details & Build Log

---

** Build的過程花生省魔術?**
* git repo被clone並依照設定找Dockerfile來build
* README.md 也被直接拿來當Docker Hub上的說明

---

** Automated Build的限制 **
* 不支援 Git Large File System (Git LFS)
* 每 5 分鐘只能 trigger build 一次, 太密集會 ignore
* 不支援 docker build 的參數 ex. --build-arg
* 不支援新的 multi-stage build
* https://github.com/docker/hub-feedback/issues/519#issuecomment-168652934
    
```
2 hours/2 GB RAM/1 CPU/30 GB Disk Space
```

---

** 個人心得 **
* security
* base image
* running containers
* gjchen/php7 [![](https://images.microbadger.com/badges/image/gjchen/php7.svg)](https://microbadger.com/images/gjchen/php7 "Get your own image badge on microbadger.com")

---

THE END
=======

