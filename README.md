# Rotura_Skill

Bộ kỹ năng xử lý bài toán toán học gồm 3 bước: chuẩn hóa đề bài, đánh giá đáp án, và định dạng lời giải theo đúng mẫu nộp bài.

## Tổng quan

Repo này cung cấp các prompt (system instructions) cho 3 kỹ năng:

- **Normalize Problem**: Chuẩn hóa đề bài LaTeX và phân loại lĩnh vực.
- **Evaluate Responses**: So sánh và đánh giá đáp án của mô hình với đáp án đúng.
- **Format Solution**: Định dạng lời giải theo mẫu nộp bài.

Mỗi kỹ năng đọc từ thư mục `input/` và ghi kết quả sang `output/`.

## Cấu trúc thư mục

```
Rotura_Skill/
	.gemini/                 # Prompt cho Gemini CLI
	1.normalize-problem/     # Mô tả kỹ năng 1
	2.evaluate-responses/    # Mô tả kỹ năng 2
	3.format-solution/       # Mô tả kỹ năng 3
	SAMPLE_WORKSPACE/        # Ví dụ input/output mẫu
```

## Sử dụng nhanh (Claude, Copilot, Gemini)

Bạn có thể dùng cùng một nội dung prompt cho cả Claude, Copilot và Gemini.

## Hướng dẫn từng kỹ năng

### 1) Normalize Problem

- **Input**: `input/problem.md`
- **Output**: `output/problem.md`
- **Mục tiêu**:
	- Chuẩn hóa LaTeX (inline `$...$`, display `$$...$$`).
	- Thay ký tự Unicode bằng lệnh LaTeX tương ứng.
	- Phân loại **Domain/Sub-domain** theo taxonomy trong [1.normalize-problem/SKILL.md](1.normalize-problem/SKILL.md).
	- Viết đoạn giải thích 3-5 câu theo khuôn.

### 2) Evaluate Responses

- **Input**:
	- `input/problem.md`
	- `input/solution.md`
	- `input/response1.md`
	- `input/response2.md`
- **Output**:
	- `output/response1_check.md`
	- `output/response2_check.md`
- **Mục tiêu**:
	- Đánh giá từng response **từng cái một** (không đọc cả hai response cùng lúc).
	- Kiểm tra đáp án cuối có trùng/tương đương đáp án đúng hay không.
	- Rà soát từng bước suy luận, chỉ rõ lỗi hoặc bước thiếu.

### 3) Format Solution

- **Input**: `input/solution.md`
- **Output**: `output/solution.md`
- **Mục tiêu**:
	- Chuẩn hóa cú pháp LaTeX, **không** đổi nội dung toán học.
	- Chia bước theo `Step N:` và bước cuối kết thúc bằng `Final Answer: $\boxed{<answer>}$`.
	- Thêm mục **Answer** và **Classification** theo mẫu.

## Ví dụ mẫu

Thư mục [SAMPLE_WORKSPACE](SAMPLE_WORKSPACE) chứa bộ dữ liệu mẫu:

- `SAMPLE_WORKSPACE/input/` có `problem.md`, `solution.md`, `response1.md`, `response2.md`.
- `SAMPLE_WORKSPACE/output/` có kết quả mong đợi.

Bạn có thể copy bộ input mẫu này vào thư mục `input/` để test nhanh.

## Lưu ý

- Mỗi kỹ năng có file mô tả chi tiết trong:
	- [1.normalize-problem/SKILL.md](1.normalize-problem/SKILL.md)
	- [2.evaluate-responses/SKILL.md](2.evaluate-responses/SKILL.md)
	- [3.format-solution/SKILL.md](3.format-solution/SKILL.md)
- Dùng đúng định dạng output chính xác theo mẫu trong SKILL.md để tránh sai lệch.
