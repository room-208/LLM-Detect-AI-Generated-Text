# LLM-Detect-AI-Generated-Text

## Dataset

それぞれの`prompt`に対するサンプル数をまとめる
| prompt | human | gpt-3.5 | gpt-4 | llama-7b | llama-70b | falcon-180b | mistral-7b | claude |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| `Phones and driving` |
| `Car-free cities` | 708[^1] | 250[^2] | 100[^2] |
| `Summer projects` |
| `"A Cowboy Who Rode the Waves"` |
| `Mandatory extracurricular activities` |
| `Exploring Venus` |
| `Facial action coding system` |
| `The Face on Mars` |
| `Community service` |
| `Grades for extracurricular activities` |
| `Driverless cars` |
| `Does the electoral college work?` | 670[^1] | 250[^2] | 100[^2] |
| `Cell phones at school` |
| `Distance learning` |
| `Seeking multiple opinions` |

[^1]:[llm-detect-ai-generated-text](https://www.kaggle.com/competitions/llm-detect-ai-generated-text/data)
[^2]:[llm-generated-essays](https://www.kaggle.com/datasets/radek1/llm-generated-essays/)
[^3]:[daigt-external-dataset](https://www.kaggle.com/datasets/alejopaullier/daigt-external-dataset/)
[^4]:[daigt-data-llama-70b-and-falcon180b](https://www.kaggle.com/datasets/nbroad/daigt-data-llama-70b-and-falcon180b/)
[^5]:[daigt-proper-train-dataset](https://www.kaggle.com/datasets/thedrcat/daigt-proper-train-dataset/)
[^6]:[hello-claude-1000-essays-from-anthropic](https://www.kaggle.com/datasets/darraghdog/hello-claude-1000-essays-from-anthropic/)
[^7]:[llm-7-prompt-training-dataset](https://www.kaggle.com/datasets/carlmcbrideellis/llm-7-prompt-training-dataset/)
[^8]:[persaude-corpus-2](https://www.kaggle.com/datasets/nbroad/persaude-corpus-2/)

## Leadear Board Probing

### Prompt 探索

[PERSUADE 2.0](https://www.kaggle.com/datasets/nbroad/persaude-corpus-2)の`prompt_name`ごとの上昇幅を確認します。（サンプル数の比率やvalidationをしていないので、する必要はあるかもしれない。）
| prompt | [LB Probing With Xgboost](https://www.kaggle.com/code/room208/lb-probing-with-xgboost/notebook) | [LB Probing With LogisticRegression](https://www.kaggle.com/code/room208/lb-probing-with-logisticregression/notebook) |
| ---- | ---- | ---- |
| `追加なし` | 0.599 | 0.630 |
| `Phones and driving` |
| `Car-free cities` | - | - |
| `Summer projects` |
| `"A Cowboy Who Rode the Waves"` |
| `Mandatory extracurricular activities` |
| `Exploring Venus` |
| `Facial action coding system` |
| `The Face on Mars` |
| `Community service` |
| `Grades for extracurricular activities` |
| `Driverless cars` |
| `Does the electoral college work?` | - | - |
| `Cell phones at school` |
| `Distance learning` |
| `Seeking multiple opinions` |

### 人間と機械の比率の探索
