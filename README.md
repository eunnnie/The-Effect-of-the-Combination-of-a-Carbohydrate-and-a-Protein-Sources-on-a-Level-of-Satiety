
## 📌 Project Summary | 프로젝트 요약

- **📅 Date**: August 21, 2020  
- **🛠 Tool | 도구**:  
  - R (FrF2 패키지를 활용한 실험설계 분석)  
- **🧪 Design | 설계**:  
  - Full Factorial Design (2 factors × 2 levels)  
  - 탄수화물(carbohydrate) × 단백질(protein) 조합 실험 (총 4가지 조합)  
  - 각 조합은 2회 반복 (replicated twice)  
- **🎯 Goal | 목표**:  
  - Identify which food combination produces the highest level of satiety  
  - **포만감을 가장 오래 지속시키는 탄수화물+단백질 조합을 찾는 것**

---

## 📊 Variables | 변수 설명

| 변수 (Variable) | 설명 (Description) |
|------------------|--------------------|
| Carbohydrate Source | Pumpkin or Sweet Potato (150g) |
| Protein Source       | Egg (3) or Chicken Breast (100g) |
| Satiety Level        | 1 to 5 scale, recorded 4 hours after meal |
|                     | 1 = Very hungry ~ 5 = Very full |

---

## 🔍 Methodology | 분석 방법

- **Experimental Design | 실험 설계**  
  - 2×2 요인설계 (Full Factorial Design)  
  - 각 요인(탄수화물, 단백질)의 주효과(main effect) 및 상호작용(interaction effect) 분석  
  - 사용 도구: `FrF2` 패키지를 통한 설계 및 분석

- **Analysis | 분석 방식**
  - 평균 포만감(satiety) 비교  
  - Interaction Plot 및 ANOVA 분석 수행  

---

## 📈 Key Findings | 주요 결과

- 고구마 + 닭가슴살 조합이 가장 높은 포만감을 유도  
- 두 요인 간 유의한 상호작용(interaction)이 존재함  
- 단일 음식보다 **조합의 시너지**가 중요한 변수로 작용

---

## 🧠 Interpretation | 해석 (강조)

- 🍠🥚 **탄수화물과 단백질 조합의 차이에 따라 포만감이 크게 달라짐**  
- 💡 고구마는 복합탄수화물로 소화가 느려 포만감 유지에 유리  
- 💪 닭가슴살은 고단백 식품으로, 소화 속도를 늦추고 포만감을 증대  
- ➕ 이 두 식품의 조합은 **상호작용 효과**를 통해 포만감을 극대화함

---

## 🧾 Conclusion | 결론 (강조)

- ✅ **Sweet Potato + Chicken Breast 조합**이 포만감을 가장 오래 유지함  
- ✅ 실험 설계를 통해 **식단 구성의 과학적 최적화 가능성** 확인  
- 📌 향후 체중 감량 및 식이 요법 시 **실험기반 식단 설계의 중요성** 강조  
- 📌 건강한 식단은 단일 식품보다는 **전략적 조합**이 핵심임
