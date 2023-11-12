# LLM-Detect-AI-Generated-Text

## Dataset

それぞれの`prompt`に対するサンプル数をまとめる。ただし、[llm-detect-ai-generated-text](https://www.kaggle.com/competitions/llm-detect-ai-generated-text/data)と[persaude-corpus-2](https://www.kaggle.com/datasets/nbroad/persaude-corpus-2/)には重複した文が存在することに注意する。
| prompt | human | gpt-3.5 | gpt-4 | llama-70b | falcon-180b | claude | mistral-7b |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| `Phones and driving` | 1168[^8] | | | 37[^4] | 29[^4] | 69[^6] |
| `Car-free cities` | 708[^1] + 1959[^8] | 250[^2] | 100[^2] | 39[^4] | 35[^4] | 49[^6] |
| `Summer projects` | 1750[^8] | | | 34[^4] | 26[^4] | 60[^6] |
| `"A Cowboy Who Rode the Waves"` | 1372[^8] | | | 28[^4] | 31[^4] | 73[^6] |
| `Mandatory extracurricular activities` | 1670[^8] | | | 36[^4] | 28[^4] | 78[^6] |
| `Exploring Venus` | 1862[^8] | | | 31[^4] | 33[^4] | 64[^6] |
| `Facial action coding system` | 2167[^8] | | | 34[^4] | 35[^4] | 70[^6] |
| `The Face on Mars` | 1583[^8] | | | 36[^4] | 29[^4] | 70[^6] |
| `Community service` | 1542[^8] | | | 32[^4] | 28[^4] | 53[^6] |
| `Grades for extracurricular activities` | 1626[^8] | | | 37[^4] | 27[^4] | 64[^6] |
| `Driverless cars` | 1886[^8] | | | 38[^4] | 24[^4] | 69[^6] |
| `Does the electoral college work?` | 670[^1] + 2046[^8] | 250[^2] | 100[^2] | 31[^4] | 25[^4] | 74[^6] |
| `Cell phones at school` | 1656[^8] | | | 24[^4] | 32[^4] | 64[^6] |
| `Distance learning` | 2157[^8] | | | 44[^4] | 33[^4] | 66[^6] |
| `Seeking multiple opinions` | 1552[^8] | | | 32[^4] | 36[^4] | 77[^6] |
| `PERSUADE 2.0 以外` | | 2421[^3](or gpt-4) | | 659[^4] | 604[^4] |

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
| `Phones and driving` | 0.548 | 0.628 |
| `Car-free cities` | - | - |
| `Summer projects` | 0.579 | 0.607 |
| `"A Cowboy Who Rode the Waves"` | TBD | 0.679 |
| `Mandatory extracurricular activities` | TBD | 0.643 |
| `Exploring Venus` | TBD | 0.643 |
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
