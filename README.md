# 📁 Vào thư mục dự án (sửa lại đường dẫn nếu cần)
cd /d/GitHub/bs_Loan

# 🔀 Tạo và chuyển sang nhánh mới nếu chưa có
git checkout -b liem_feature

# 🔄 Cập nhật từ nhánh chính trước khi làm
git checkout main
git pull origin main
git checkout liem_feature
git merge main

# 🛠️ Làm việc bình thường trong RStudio / Quarto...

# 💾 Lưu thay đổi
git add .
git commit -m "BS Liêm: cập nhật phân tích mới"
git push origin liem_feature

# 🌐 Tạo Pull Request trên GitHub từ liem_feature → main
# 👉 Vào https://github.com/[tài khoản]/bs_Loan/pulls và nhấn 'New pull request'

# ✅ Sau khi đã Merge Pull Request:
git checkout main
git pull origin main
git branch -d liem_feature  # (Tuỳ chọn) Xoá nhánh local nếu không cần nữa


