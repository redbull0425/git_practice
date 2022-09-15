出處: [https://gitbook.tw/chapters/using-git/ignore](https://gitbook.tw/chapters/using-git/ignore)
不只是比較機密的檔案，有時候一些程式編譯的中間檔或暫存檔，
因為每次只要一編譯就等於產生一次新的檔案，對專案來說通常沒有實質的利用價值，
像這樣的檔案其實也不會想讓它進到 Git 裡。

要做到這件事，只要在專案目錄裡放一個 .gitignore 檔案，
並且設定想要忽略的規則就行了。如果這個檔案不存在，就手動新增它：

# command
$ touch .gitignore
---
然後編輯這個檔案的內容：

# 檔案名稱 .gitignore

# 忽略 secret.yml 檔案
secret.yml

# 忽略 config 目錄下的 database.yml 檔案
config/database.yml

# 忽略所有 db 目錄下附檔名是 .sqlite3 的檔案
/db/*.sqlite3

# 忽略所有附檔名是 .tmp 的檔案
*.tmp

# 當然你要忽略自己也可以，只是通常不會這麼做
# .gitignore
只要 .gitignore 這個檔案存在，即使這個檔案沒被 Commit 或是沒被 Push 上 Git Server 就會有效果。
但這個檔案會建議 Commit 進專案並且推上 Git Server，這樣一來整個專案一起開發的人可以共享相同的設定。

