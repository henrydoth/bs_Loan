- [gitignore](#gitignore)
- [=== RStudio project files ===](#-rstudio-project-files-)
- [=== Quarto output ===](#-quarto-output-)
- [=== Dữ liệu \& file tạm ===](#-dữ-liệu--file-tạm-)
- [=== Word documents dùng để nhập nội dung ===](#-word-documents-dùng-để-nhập-nội-dung-)
- [=== Bỏ qua toàn bộ file trong thư mục source/ ngoại trừ .bib ===](#-bỏ-qua-toàn-bộ-file-trong-thư-mục-source-ngoại-trừ-bib-)
- [=== Hình ảnh \& thư mục cache ===](#-hình-ảnh--thư-mục-cache-)
- [=== Thư mục backup ===](#-thư-mục-backup-)
- [=== Jupyter notebooks (tuỳ chọn nếu dùng Python) ===](#-jupyter-notebooks-tuỳ-chọn-nếu-dùng-python-)
- [🧠 Git \& GitHub Cheat Sheet cho nhóm bs\_Loan (Quarto + R)](#-git--github-cheat-sheet-cho-nhóm-bs_loan-quarto--r)
  - [🛠️ 1. Khởi tạo dự án Git (chỉ 1 lần duy nhất)](#️-1-khởi-tạo-dự-án-git-chỉ-1-lần-duy-nhất)
  - [👥 2. Thiết lập Git người dùng (cho từng máy)](#-2-thiết-lập-git-người-dùng-cho-từng-máy)
  - [🌿 3. Tạo và làm việc với nhánh](#-3-tạo-và-làm-việc-với-nhánh)
    - [Tạo nhánh mới từ main](#tạo-nhánh-mới-từ-main)
    - [Push nhánh mới lên GitHub](#push-nhánh-mới-lên-github)
  - [🔁 4. Gộp (merge) nhánh về main (có quyền)](#-4-gộp-merge-nhánh-về-main-có-quyền)
  - [🧹 5. Xoá nhánh](#-5-xoá-nhánh)
    - [Xoá cục bộ:](#xoá-cục-bộ)
    - [Xoá trên GitHub:](#xoá-trên-github)
  - [🧪 6. Kiểm tra trạng thái](#-6-kiểm-tra-trạng-thái)
  - [🔄 7. Cập nhật `.gitignore` đúng chuẩn](#-7-cập-nhật-gitignore-đúng-chuẩn)
- [=== RStudio files ===](#-rstudio-files-)
- [=== Quarto outp](#-quarto-outp)

## 📁 `.gitignore` Cheat Sheet cho Dự án Quarto + R + Word

# gitignore
# === RStudio project files ===
.Rproj.user/
.Rhistory
.RData
.Ruserdata
*.Rproj

# === Quarto output ===
_output/
bs_loan_quarto_output_files/
*.docx
*.pdf
*.html

# === Dữ liệu & file tạm ===
*.csv
*.sav

# === Word documents dùng để nhập nội dung ===
*.docx

# === Bỏ qua toàn bộ file trong thư mục source/ ngoại trừ .bib ===
source/*
source/**
!source/
!source/*.bib

# === Hình ảnh & thư mục cache ===
image/tmp/
image/pdf/
image/png/
.Rcache/
_cache/
__pycache__/

# === Thư mục backup ===
bak/

# === Jupyter notebooks (tuỳ chọn nếu dùng Python) ===
*.ipynb
.ipynb_checkpoints/
```

👉 **Lưu ý**: Nếu bạn đã commit các file cần ignore trước đó, chạy lệnh sau để xóa chúng khỏi Git nhưng giữ lại trên máy:

```bash
git rm --cached đường/dẫn/tệp
git commit -m "Remove tracked file as per .gitignore"
git push
```

📌 Ví dụ:

```bash
git rm --cached source/ama-brackets.csl
git rm --cached source/sstt_dtcs_quato_words_input.docx
```
# 🧠 Git & GitHub Cheat Sheet cho nhóm bs_Loan (Quarto + R)

---

## 🛠️ 1. Khởi tạo dự án Git (chỉ 1 lần duy nhất)
```bash
git init
git remote add origin https://github.com/<user>/bs_Loan.git
git add .
git commit -m "Initial commit"
git push -u origin main
```

---

## 👥 2. Thiết lập Git người dùng (cho từng máy)

```bash
git config --global user.name "bs_li"
git config --global user.email "liem20k@gmail.com"
```

Hoặc với user khác:
```bash
git config --global user.name "bs_hu"
git config --global user.email "tollyhenry@gmail.com"
```

---

## 🌿 3. Tạo và làm việc với nhánh

### Tạo nhánh mới từ main
```bash
git checkout main
git pull
git checkout -b lo_branch1
```

### Push nhánh mới lên GitHub
```bash
git push -u origin lo_branch1
```

---

## 🔁 4. Gộp (merge) nhánh về main (có quyền)

```bash
git checkout main
git pull origin main
git merge lo_branch1
git push origin main
```

---

## 🧹 5. Xoá nhánh

### Xoá cục bộ:
```bash
git branch -d lo_branch1
```

### Xoá trên GitHub:
```bash
git push origin --delete lo_branch1
```

---

## 🧪 6. Kiểm tra trạng thái

```bash
git status
git log --oneline --graph --all
```

---

## 🔄 7. Cập nhật `.gitignore` đúng chuẩn

```gitignore
# === RStudio files ===
.Rproj.user/
.Rhistory
.RData
.Ruserdata
*.Rproj

# === Quarto outp
