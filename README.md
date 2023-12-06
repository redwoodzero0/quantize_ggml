# ggml 양자화
ggml 및 llama.cpp로 라마 모델 양자화하기



    q2_k: attention.vw 및 feed_forward.w2 텐서에는 Q4_K를, 다른 텐서에는 Q2_K를 사용합니다.
    q3_k_l: attention.wv, attention.wo, feed_forward.w2 텐서에는 Q5_K를 사용하고, 그 외에는 Q3_K를 사용합니다.
    q3_k_m: attention.wv, attention.wo, feed_forward.w2 텐서에는 Q4_K를 사용하고, 그 외에는 Q3_K를 사용합니다.
    q3_k_s: 모든 텐서에 Q3_K 사용.
    q4_0: 기본 양자화 방식, 4비트.
    q4_1: q4_0보다 정확도가 높지만 q5_0만큼 높지는 않습니다. 하지만 q5 모델보다 추론 속도가 빠릅니다.
    q4_k_m: attention.wv 및 feed_forward.w2 텐서의 절반에는 Q6_K를 사용하고, 그 외에는 Q4_K를 사용합니다.
    q4_k_s: 모든 텐서에 Q4_K 사용.
    q5_0: 더 높은 정확도, 더 많은 리소스 사용, 더 느린 추론.
    q5_1: 정확도, 리소스 사용량, 추론 속도는 더욱 향상되었습니다.
    q5_k_m: attention.wv 및 feed_forward.w2 텐서의 절반에 Q6_K를 사용하고, 그 외에는 Q5_K를 사용합니다.
    q5_k_s: 모든 텐서에 Q5_K 사용.
    q6_k: 모든 텐서에 Q6_K 사용.
    q8_0: float16과 거의 구별할 수 없습니다. 리소스 사용량이 많고 느립니다. 대부분의 용도로는 권장되지 않습니다.


Credit : Maxime Labonne
