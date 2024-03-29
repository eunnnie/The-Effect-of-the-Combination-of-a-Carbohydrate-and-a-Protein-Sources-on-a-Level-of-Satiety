# 탄수화물원과 단백질원의 조합이 포만감에 미치는 영향
다이어터의 궁금증: 어떤 식품을 통해 탄수화물과 단백질을 섭취했을 때 가장 포만감이 높을까요? <br>
우리는 해답을 얻기 위해 직접 실험을 설계했습니다! 
## 방법
$2^{2}$ 설계로 요인의 수가 2개이고, 각 요인마다 수준수가 2개인 요인실험을 진행했습니다. (아래 표 참고) <br>
![무제](https://user-images.githubusercontent.com/90596549/236738214-b6eaf022-4b83-4b2b-894b-2c54f672870c.png)
<br>
- 각각의 조합으로 점심식사 후, 포만감을 1점 (매우 배고픔)에서 5점 (매우 배부름) 사이의 점수로 기록했습니다. <br>
- 실험이 진행된 8일 동안 어느날 어떤 조합으로 식사할지는 R을 이용해 임의 선택되었고, 아침식사와 저녁식사는 철저히 통제되었습니다.<br> 
(매일 같은 샐러드만 먹었어요 ㅜㅜ) <br>
## 데이터 분석 
### 탄수화물원과 단백질원 조합에 대한 입방체도 
![cp](https://user-images.githubusercontent.com/90596549/236738671-ec0d733a-a792-4aa0-a1a5-585450960966.png)

- 실험에서 사용된 단백질원의 종류가 두개밖에 없어서 사실 예쁜 입방체도를 만들 수 없었습니다. <br> 
- 따라서 단백질원을 중복해서 입력하므로 예쁜 입방체도를 얻었고, 해석을 위해 맨 윗면은 무시해도 좋습니다. <br>
- 입방체도의 프로틴 모서리의 (1, -1)은 각각 닭가슴살과 삶은 계란을 의미하고, 탄수화물 모서리의 (1, -1)은 각각 고구마와 단호박을 의미합니다. <br>
- 조합별 포만감 점수를 내림차순으로 나열하면 (고구마, 닭가슴살, 점수: 4.5), (단호박, 닭가슴살, 점수: 3.5), (고구마, 계란, 점수: 3), (단호박, 계란, 점수: 2) 이 됩니다. <br>

### 탄수화물과 단백질의 교호작용 그래프 
![ip](https://user-images.githubusercontent.com/90596549/236738697-207376fd-8445-4954-b8a3-556a12dbbb51.png)

- 교호작용 그래프를 통해 탄수화물과 단백질의 교호작용이 없음을 확인했습니다. 

### 상관계수표
<img width="372" alt="cef" src="https://user-images.githubusercontent.com/90596549/236738736-8280b612-31f0-4c4e-8f45-51cb0a570b05.png">
- intercept는 본 실험에서 무의미하므로 무시해도 좋습니다. <br>

#### 계수 추정값의 해석
- 탄수화물 요인의 주효과에 대해 추정된 계수를 통해 단호박에서 고구마로 탄수화물원만 변경한다면 포만감 점수가 1점 높아진다는 것을 알 수 있습니다. <br>
- 단백질 요인의 주효과에 대해 추정된 계수를 통해 삶은계란에서 닭가슴살로 단백질원만 변경하면 포만감 점수가 1.5점 높아진다는 것을 알 수 있습니다. <br>

#### P-value의 해석 및 가설검정
귀무 가설은 탄수화물 요인의 주효과와 단백질 요인의 주효과 계수가 0으로, 식품종류와 포만감 점수 간에 연관성이 없다는 것을 나타냅니다. <br> 
실험에선 0.05를 유의 수준으로 설정했습니다. 이는 실제로 연관성이 없는데 연관성이 존재한다는 결론을 내릴 위험이 5%라는 것을 나타냅니다. <br>
##### 탄수화물 요인의 주효과
- $(Pr(>|t|)=0.09) > 0.05$는 탄수화물 요인의 주효과에 대한 p-value가 유의 수준보다 높다는 것을 나타냅니다. <br>
- 따라서 귀무가설을 기각할 수 없고, 탄수화물원의 종류와 포만감점수 사이에 통계적으로 유의한 연관성이 있다는 결론을 내릴 수 없습니다.<br>
##### 단백질 요인의 주효과
- $(Pr(>|t|)=0.03) < 0.05$는 단백질 요인의 주효과에 대한 p-value가 유의 수준보다 낮다는 것을 나타냅니다. <br>
- 따라서 귀무가설을 기각하고, 단백질원의 종류와 포만감점수 사이에 통계적으로 유의한 연관성이 있다는 결론을 내릴 수 있습니다.<br>
##### 탄수화물 요인과 단백질 요인 사이의 교호작용효과
- $(Pr(>|t|)=2.00) > 0.05$는 탄수화물 요인과 단백질 요인 사이의 교호작용효과에 대한 p-value가 유의 수준보다 높다는 것을 나타냅니다. <br>
- 따라서 귀무가설을 기각할 수 없고, 탄수화물원과 단백질원 사이의 교호작용이 존재한다는 통계적으로 유의한 증거가 없다는 결론을 내릴 수 있습니다.<br>

### 결론
- 우리는 실험을 통해 포만감 정도에 탄수화물의 종류는 크게 상관이 없다는 것을 알게 됐습니다. <br>
- 그러나, 동량의 단백질을 섭취한다는 가정하에 닭가슴살이 계란보다는 더 높은 포만감을 준다는 것이 확인됐군요. <br>
- 역시 다이어터들이 닭가슴살을 주로 먹는건 다 이유가 있나 봅니다. 
- 그럼 저는 닭가슴살과 고구마, 단호박을 먹으며 여름을 준비해볼게요! 다들 건강합시다!

### 앞으로
- 더 많은 식품군으로 포만감 실험을 해봐야겠습니다. 
- 실험기간이 너무 짧은 것 같습니다. 긴 시간동안 실험을 하면 어떤 결과가 나올지 궁금합니다. 
- 3대 영양소는 탄수화물, 단백질, 지방을 모두 고려해서 실험해보는 것도 의미가 있을 것 같아요. 
- 포만감 점수는 너무 주관적인 지표라서 좀 더 과학적인 접근 (혈당지수 등.)이 필요할 것 같습니다. 


