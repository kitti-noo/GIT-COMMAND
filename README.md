# GIT command
## git config
- git config -–global user.email "[email address]" 
- git config -–global user.name "[user name]"
- git config --global --edit : แก้ไข user และ email
## git init : เริ่มต้นการใช้งาน git ใน directory
- git init
## git status : ตรวจสอบสถานะ
- git status
## git add : เพิ่มไฟล์เข้าสู่ staged status
- git add [path]
- git add . : เพิ่มไฟล์ทั้งหมด
## git commit 
- git commit -m "text"
- git commit -a : commit ทั้งหมด
- git commit -am "text"
## git remote
- git remote add origin [URL]
- git remote -v : ตรวจสอบ remote
- git remote remove origin : ลบ remote origin
## git push : การส่ง commit ที่ Local Repository ไปยัง Remote Repository
- git push -u origin [brand name]
- git push -f


## git clone : การเอางานที่เราต้องการลงมาไว้ที่เครื่องเรา (ใช้กรณีที่ไม่เคยมี Repository นั้นมาก่อน)
- git clone [URL]
## ลบ git init จาก directory
- rm -rf .git*
## git diff : รีวิวไฟล์ที่แก้ไปแล้ว (สถานะ modified) ผ่าน diff view
- git diff --staged :  diff ไฟล์ที่ add แล้ว (สถานะ staged) แต่ยังไม่ได้ commit
## git reset : เอาไฟล์ที่ add ไปแล้วออกมาจาก staged ให้กลับมาเป็น modified
- git reset
## git log out 
- git config --global --unset user.name
- git config --global --unset user.email
- git config --global --unset credential.helper
- git config --global --unset-all 
## git pull : การดึง Remote Repository ไฟล์มายัง Local Repository เพื่อทำการอัพเดต 
- git pull origin [branch name]
# SSH key 
- ssh-keygen -t rsa -b 4096 -C "your_email@example.com" หรือ  ssh-keygen -o
- cat ~/.ssh/id_rsa.pub 
- copy ข้อความไปใส่ใน Setting --> SSH keys
## Git Hard Reset to old version
- git reset --hard HEAD       (going back to HEAD)
- git reset --hard HEAD^      (going back to the commit before HEAD)
- git reset --hard HEAD~1     (equivalent to "^")
- git reset --hard HEAD~2     (going back two commits before HEAD)
- git reset --hard 0ad5a7a6   (going back to 0ad5a7a6)
