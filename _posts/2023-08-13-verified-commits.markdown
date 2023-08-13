---
layout: post
title:  "Verified Commits - GPG"
date:   2023-08-13 10:19:19 +0530
categories: git gpg
---

# List Keys

```
gpg --list-secret-keys --keyid-format=long
```

The result

```
praveen@lk:~/host-repo$ gpg --list-secret-keys --keyid-format=long
/home/praveen/.gnupg/pubring.kbx
--------------------------------
sec   rsa3072/5FC284DF2BEEBB57 2023-05-13 [SC]
      59089308690F5XXXXX8482235FC284DF2BXXXB57
uid                 [ultimate] Praveen Dias (Praveen's GPG Key) <praveendias1180@gmail.com>
ssb   rsa3072/XXXXDC837C75ADEB 2023-05-13 [E]
```