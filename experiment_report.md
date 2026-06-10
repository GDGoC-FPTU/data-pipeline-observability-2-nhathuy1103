# Experiment Report: Data Quality Impact on AI Agent

**Student ID:** 2A202600731
**Name:** Tran Nhat Huy
**Date:** 2026-06-10

---

## 1. Ket qua thi nghiem

Chay `agent_simulation.py` voi 2 bo du lieu va ghi lai ket qua:

| Scenario | Agent Response | Accuracy (1-10) | Notes |
|----------|----------------|-----------------|-------|
| Clean Data (`processed_data.csv`) | Agent chon Laptop voi gia $1200. | 10 | Du lieu da duoc validate va transform; ket qua phu hop voi logic chon san pham electronics co gia cao nhat. |
| Garbage Data (`garbage_data.csv`) | Agent chon Nuclear Reactor voi gia $999999. | 1 | Outlier khong hop ly van duoc agent xem la lua chon tot nhat. |

---

## 2. Phan tich & nhan xet

### Tai sao Agent tra loi sai khi dung Garbage Data?

Agent khong tu danh gia chat luong hay y nghia thuc te cua du lieu. No chi loc
category electronics va chon record co price cao nhat, vi vay outlier Nuclear
Reactor voi gia 999999 chiem uu the va tao ra cau tra loi sai. Duplicate ID co
the lam agent nham lan danh tinh san pham; sai kieu du lieu co the gay loi khi
so sanh hoac tinh toan; null values lam mat thong tin can thiet. Neu cac record
nay duoc dua vao he thong truy xuat ma khong validate, agent se coi chung la
su that. Vi the pipeline can kiem tra schema, kieu du lieu, gia tri bat thuong,
tinh duy nhat va truong bat buoc truoc khi du lieu duoc dung boi agent.

---

## 3. Ket luan

**Quality Data > Quality Prompt?** Dong y. Prompt tot co the huong dan cach tra
loi, nhung khong the sua mot outlier hoac gia tri sai ma agent tin la dung.
Kiem soat chat luong du lieu la dieu kien can de agent tao ket qua dang tin cay.
