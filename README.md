[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=24112913&assignment_repo_type=AssignmentRepo)
# Day 10 Lab: Data Pipeline & Data Observability

**Student Email:** nhathuyit1103@gmail.com
**Student ID:** 2A202600731
**Name:** Trần Nhất Huy

---

## Mo ta

Xây dựng ETL pipeline tự động để đọc dữ liệu sản phẩm từ JSON, loại bỏ dữ liệu không hợp lệ, chuẩn hóa danh mục, tính giá giảm 10%, thêm thời gian xử lý và xuất kết quả ra CSV. Đồng thời thực hiện stress test để đánh giá ảnh hưởng của dữ liệu rác đến kết quả trả lời của AI Agent.
---

## Cach chay (How to Run)

### Prerequisites
```bash
pip install pandas
```

### Chay ETL Pipeline
```bash
python solution.py
```

### Chay Agent Simulation (Stress Test)
```bash
# Bước 1: Tạo file processed_data.csv từ dữ liệu sạch
python solution.py

# Bước 2: Tạo file garbage_data.csv chứa dữ liệu rác
python generate_garbage.py

# Bước 3: Chạy và so sánh kết quả Clean Data với Garbage Data
python agent_simulation.py
```

---

## Cau truc thu muc

```
├── solution.py              # ETL Pipeline script
├── processed_data.csv       # Output cua pipeline
├── experiment_report.md     # Bao cao thi nghiem
└── README.md                # File nay
```

---

## Ket qua

Pipeline đã đọc 5 records từ raw_data.json, giữ lại 3 records hợp lệ và loại bỏ 2 records không hợp lệ. Dữ liệu sau xử lý được chuẩn hóa category, tính giá giảm 10%, thêm thời gian xử lý và lưu vào processed_data.csv.
