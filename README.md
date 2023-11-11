# LLM-Detect-AI-Generated-Text

## Dataset

| prompt | human | gpt-3.5 | gpt-4 | llama-7b | llama-70b | falcon-180b | mistral-7b | claude |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| `Car-free cities` |
| `Does the electoral college work?` |
| `Exploring Venus` |
| `The Face on Mars` |
| `Facial action coding system` |
| `A Cowboy Who Rode the Waves` |
| `Driverless cars` |

## Leadear Board Probing
[LB Probing With Xgboost](https://www.kaggle.com/code/room208/lb-probing-with-xgboost/edit)のノートブックで確認してます。`PERSUADE 2.0`の`prompt_name`ごとの上昇幅を確認します。
| prompt | score |
| ---- | ---- |
| `追加なし` | 0.599 |
| `Phones and driving` | 0.579 |
| `Car-free cities` + `Does the electoral college work?` | 0.524 |
| `Summer projects` | 0.602 |
| `"A Cowboy Who Rode the Waves"` | 0.590 |
| `Mandatory extracurricular activities` |
| `Exploring Venus` | 0.621 |
| `Facial action coding system` | 0.606 |
| `The Face on Mars` | 0.606 |
| `Community service` |
| `Grades for extracurricular activities` |
| `Driverless cars` |
| `Cell phones at school` |
| `Distance learning` |
| `Seeking multiple opinions` |
