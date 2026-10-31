# Source documents and evaluation set

## `source_documents_68.txt`

The 68 public Indonesian documents of the knowledge base, with code, domain, type, title, page count and file name. The full PDF files are available on [Google Drive](https://drive.google.com/drive/folders/1XUAsv2chiUNKnqNzQbnOm-uvxOwHuz7X?usp=sharing).

| Domain | Documents |
|---|---|
| Waqf | 45 |
| Zakat, infaq and sadaqah | 18 |
| Qurban | 5 |

Regulatory documents (41) are statutes, government regulations, BWI and BAZNAS regulations, and MUI/DSN-MUI fatwas. Literacy documents (27) are BWI educational articles and guidebooks.

## `evaluation_qa_50.xlsx`

The 50 evaluation questions (in Indonesian), balanced by domain (waqf 13, zakat 13, infaq-sadaqah 12, qurban 12) and difficulty (low 16, medium 17, high 17).

| Column | Description |
|---|---|
| `id` | Question ID |
| `domain` | waqf, zakat, infaq-sadaqah or qurban |
| `difficulty` | low, medium or high |
| `question` | Question |
| `reference_answer` | Reference answer, validated by domain experts |
| `source_quotes` | Verbatim quotes from the corpus that support the reference answer |
| `source_location` | Document and page of each quote |
