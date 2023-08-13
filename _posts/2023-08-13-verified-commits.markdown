---
layout: post
title:  "Verified Commits - GPG"
date:   2023-08-13 10:19:19 +0530
categories: git gpg
---

## List Keys

```
gpg --list-secret-keys --keyid-format=long
```

# The result

```
praveen@lk:~/host-repo$ gpg --list-secret-keys --keyid-format=long
/home/praveen/.gnupg/pubring.kbx
--------------------------------
sec   rsa3072/5FC284DF2BEEBB57 2023-05-13 [SC]
      59089308690F5XXXXX8482235FC284DF2BXXXB57
uid   [ultimate] Praveen Dias (Praveen's GPG Key) <praveendias1180@gmail.com>
ssb   rsa3072/XXXXDC837C75ADEB 2023-05-13 [E]
```

## Generate Key

```
gpg --full-generate-key
```

https://docs.github.com/en/authentication/managing-commit-signature-verification/generating-a-new-gpg-key

# Unverified Commits

![](../images/08/unverified-commits.png)

# Verify Commits

```
git config --global user.signingkey 5FC284DF2BEEBB57
git config --global commit.gpgsign true
```

![](../images/08/verified-commits.png)