## 📁 `.gitignore` Cheat Sheet cho Dự án Quarto + R + Word

```gitignore
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
