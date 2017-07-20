在Docker Hub建立Automated Build Repository
=========================================
    freak@funP.com

---

https://docs.docker.com/docker-hub/builds/

---

**為什麼想使用 Docker Hub?**
* 沒資源自己架 docker registry
* 自己架了還要 maintain & upgrade

**缺點:**
* lock-in
* 不付錢的話只有一個 private repo

---

**為什麼想使用 Docker Hub?**
* 策略性的 Open 

---

**為什麼 Automated Build**
* 提高使用者對你的 repository 的信任
* ~~爽~~ 

---

**在Docker Hub上進行Automated Build的需求**
* Docker Hub Account
* host 在 GitHub 或 Bitbucket 上的 git repository