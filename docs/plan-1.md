Ôi chuẩn bài luôn 😆

Có **2 máy + 2 GitHub account** là đủ để học Git theo cách gần giống đi làm nhất rồi.

Mình sẽ học theo roadmap này:

---

## Bài 1: Git cơ bản (1 máy)

Tạo repo:

```bash
mkdir git-playground
cd git-playground

git init
```

Tạo file:

```bash
echo "hello" > app.txt
```

Xem trạng thái:

```bash
git status
```

Commit:

```bash
git add .
git commit -m "feat: add app.txt"
```

Luyện:

```bash
git log
git diff
git restore
git rm
```

---

## Bài 2: GitHub

Push lên account A:

```bash
git remote add origin ...
git push
```

Luyện:

```bash
git clone
git pull
git push
```

---

## Bài 3: 2 máy

Máy A:

```bash
echo "from machine A" >> app.txt
git commit
git push
```

Máy B:

```bash
git pull
```

Đây là workflow thật ngoài đời.

---

## Bài 4: Branch

Tạo branch:

```bash
git checkout -b feature/login
```

Commit vài lần.

Quay lại:

```bash
git checkout main
```

Merge:

```bash
git merge feature/login
```

---

## Bài 5: Conflict (quan trọng)

Máy A:

```text
hello from A
```

Máy B:

```text
hello from B
```

Cùng sửa 1 dòng.

A push.

B pull.

Boom 💥

```text
CONFLICT
```

Lúc này học:

```bash
git status
git add
git commit
```

để resolve conflict.

Đây là kỹ năng Git quan trọng nhất.

---

## Bài 6: 2 account GitHub

Account A:

```text
repo chính
```

Account B:

```text
fork
```

Học:

```bash
fork
clone
remote add upstream
fetch
pull request
```

Đây là workflow open source.

---

## Bài 7: Rebase

Tạo:

```text
main
feature/login
```

Commit trên cả hai.

Thử:

```bash
git rebase main
```

Sau khi hiểu được:

```bash
merge
vs
rebase
```

thì Git của ông đã vượt mức junior rồi 😆

---

## Bài 8: Cherry-pick

Tạo 3 commit:

```text
A
B
C
```

Lấy riêng commit B:

```bash
git cherry-pick <hash>
```

Cái này đi làm dùng khá nhiều.

---

Nếu là mình, tối nay mình sẽ làm đúng 1 project:

```text
Máy Ubuntu 26   = Dev A
Máy HP          = Dev B
GitHub          = Remote
```

rồi cố tình tạo conflict.

Học cách xử lý conflict xong là ông sẽ hiểu Git nhanh hơn đọc 10 bài tutorial. 😄
