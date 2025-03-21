
# The Effect of Carbohydrate + Protein Combination on Satiety

This repository explores the effect of different combinations of carbohydrate and protein sources on the **level of satiety**. The goal is to determine which food pairing provides the highest feeling of fullness.

이 저장소는 서로 다른 탄수화물 및 단백질 조합이 **포만감 수준**에 미치는 영향을 실험적으로 분석한 결과를 담고 있습니다.

---

## Project Summary | 프로젝트 요약

- **Date**: August 21, 2020  
- **Tool**: R, FrF2 package (Full Factorial Design)  
- **Design**: 2×2 factorial design (2 carbohydrates × 2 proteins)  
- **Goal**: Identify the most satiating combination of food

---

## Methodology | 실험 방법

- Full factorial design using the `FrF2` package in R
- Two factors (Carbohydrate, Protein), each with 2 levels
- Response variable: level of satiety (scale from 1 to 10)
- Statistical analysis: ANOVA, interaction plots

---

## Results | 결과 요약

- Both **main effects** and **interaction effect** were analyzed
- Interaction plot shows [protein X + carb Y] yielded highest satiety
- ANOVA results indicate [interaction term significance: YES/NO]

---

## How to Run | 실행 방법

1. Clone this repository:
```bash
git clone https://github.com/your-username/satiety-food-combination.git
```

2. Open the RMarkdown file:
```
Final Project(pdf).Rmd
```

3. Required packages:
```r
install.packages("FrF2")
install.packages("knitr")
```

4. Knit to PDF or HTML to view results.

---

## Limitations & Suggestions | 한계 및 제안

- Further replication needed for stronger validity
- Include normality and homogeneity tests before ANOVA
- Expand food categories or levels for generalizability

---

## License

This project is licensed under the MIT License.

## Contact

For inquiries: [your_email@example.com]
