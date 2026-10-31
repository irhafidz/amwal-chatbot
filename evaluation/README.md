# Evaluation

## Automatic evaluation (Ragas)

| File | Contents |
|---|---|
| `ragas_scores_per_answer.csv` | Every answer of the six conditions (2 generators × 3 scenarios × 50 questions) with its retrieved contexts and Ragas scores |
| `ragas_mean_per_condition.csv` | Mean score of each metric per condition (Table IV of the paper) |
| `factual_correctness_precision_recall.csv` | Factual Correctness F1 with its precision and recall per answer |
| `factual_correctness_per_domain.csv` | Mean Factual Correctness per domain |
| `factual_correctness_per_difficulty.csv` | Mean Factual Correctness per difficulty level |
| `wilcoxon_between_scenarios.csv` | Wilcoxon signed-rank tests between scenarios, paired by question (n = 50) |
| `wilcoxon_between_generators.csv` | Wilcoxon signed-rank tests between GPT-4o mini and Gemini 3.6 Flash |

Judge: DeepSeek V4.1 Flash with thinking disabled. Answer Relevancy uses text-embedding-3-small. Faithfulness and Context Recall are undefined for Scenario I (no retrieved context).

## User testing (`user-testing/`)

| File | Contents |
|---|---|
| `user_testing_responses_anonymized.xlsx` | Responses of the 30 respondents: background (A1–A6), ratings of items C1–C9 (1–5), and open answers (D1–D4). No personal data |
| `item_statistics.csv` | Mean, standard deviation and agreement per item (Table V of the paper) |
| `cronbach_alpha_if_item_deleted.csv` | Cronbach's α when each item is deleted |

Items C1–C8 are adapted from Cantador et al. (2021); C9 (clarity) follows Mastor et al. (2026).
