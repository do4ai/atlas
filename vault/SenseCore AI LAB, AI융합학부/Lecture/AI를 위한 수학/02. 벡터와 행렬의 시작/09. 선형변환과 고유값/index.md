---
title: "09. 선형변환과 고유값"
source_kind: page
source_path: ssot/pages/31ee313f58b980d68c5ad8ed9d5aeff8__SenseCore AI LAB, AI융합학부/children/lecture/32be313f58b980078dbbeed4f006f95b__Lecture/children/math/32be313f58b981e7b26fea2d45e6fa7f__AI를 위한 수학/children/32be313f58b981dfaa1ef692510e6dfa__02. 식과 방정식의 언어/children/32ce313f58b981ad9be7f3becd1be9ff__9. 선형변환과 고유값
notion_id: 32ce313f58b981ad9be7f3becd1be9ff
notion_url: https://www.notion.so/32ce313f58b981ad9be7f3becd1be9ff
parent_notion_id: 32be313f58b981dfaa1ef692510e6dfa
---
# 9강. 선형변환과 고유값

이 강의의 목표는 아래 식을 보고, 고유벡터와 고유값이 무엇인지 설명할 수 있게 되는 것입니다.

$$
Av=\lambda v
$$

이 식은 행렬 $A$가 벡터 $v$를 바꾸어도 방향은 그대로이고, 길이만 $\lambda$배가 된다는 뜻입니다.

# 1. 먼저 오늘 쓸 말을 정리하자

| 말 | 뜻 |
|---|---|
| 변환 | 한 대상을 다른 대상으로 보내는 규칙 |
| 선형변환 | 벡터 덧셈과 스칼라배 구조를 보존하는 변환 |
| 행렬변환 | 행렬을 곱해서 벡터를 다른 벡터로 보내는 변환 |
| 불변방향 | 변환 뒤에도 같은 직선 위에 남는 방향 |
| 고유벡터 | 변환 뒤에도 방향이 바뀌지 않는 영벡터가 아닌 벡터 |
| 고유값 | 고유벡터가 몇 배가 되는지를 나타내는 수 |
| 대각화 | 변환을 축별 늘림과 줄임으로 읽는 방법 |
| 특성방정식 | 고유값을 찾기 위해 세우는 방정식 |

# 2. 변환은 벡터를 다른 벡터로 보내는 규칙이다

벡터

$$
v=
\begin{bmatrix}
1 \\
2
\end{bmatrix}
$$

가 있다고 합시다.

어떤 규칙이 이 벡터를

$$
\begin{bmatrix}
2 \\
4
\end{bmatrix}
$$

로 보낸다면, 그것은 하나의 변환입니다.

변환은 입력 벡터를 받아 출력 벡터를 내보내는 규칙입니다.

# 3. 행렬은 변환으로 볼 수 있다

행렬

$$
A=
\begin{bmatrix}
2 & 0 \\
0 & 3
\end{bmatrix}
$$

와 벡터

$$
x=
\begin{bmatrix}
1 \\
1
\end{bmatrix}
$$

를 곱해 봅시다.

$$
Ax=
\begin{bmatrix}
2 & 0 \\
0 & 3
\end{bmatrix}
\begin{bmatrix}
1 \\
1
\end{bmatrix}
=
\begin{bmatrix}
2 \\
3
\end{bmatrix}
$$

입니다.

행렬 $A$는 벡터 $(1,1)$을 벡터 $(2,3)$으로 보냈습니다.

따라서 행렬은 벡터를 다른 벡터로 보내는 변환으로 볼 수 있습니다.

# 4. 선형변환은 더하기와 몇 배를 보존한다

선형변환은 두 가지 성질을 지킵니다.

첫 번째는 더하기를 보존하는 것입니다.

$$
T(u+v)=T(u)+T(v)
$$

두 번째는 몇 배를 보존하는 것입니다.

$$
T(cv)=cT(v)
$$

이 말은 변환을 먼저 하든, 벡터를 더하고 몇 배 한 뒤 변환하든 구조가 깨지지 않는다는 뜻입니다.

행렬을 곱하는 변환은 선형변환입니다.

# 5. 쉬운 행렬변환: 가로와 세로를 따로 늘리기

행렬

$$
A=
\begin{bmatrix}
2 & 0 \\
0 & 3
\end{bmatrix}
$$

를 봅시다.

벡터

$$
\begin{bmatrix}
x \\
y
\end{bmatrix}
$$

에 곱하면

$$
A
\begin{bmatrix}
x \\
y
\end{bmatrix}
=
\begin{bmatrix}
2x \\
3y
\end{bmatrix}
$$

입니다.

즉 가로 성분은 $2$배, 세로 성분은 $3$배가 됩니다.

# 6. 방향이 바뀌지 않는 벡터가 있다

위 행렬

$$
A=
\begin{bmatrix}
2 & 0 \\
0 & 3
\end{bmatrix}
$$

에 가로 방향 벡터를 곱해 봅시다.

$$
e_1=
\begin{bmatrix}
1 \\
0
\end{bmatrix}
$$

그러면

$$
Ae_1=
\begin{bmatrix}
2 & 0 \\
0 & 3
\end{bmatrix}
\begin{bmatrix}
1 \\
0
\end{bmatrix}
=
\begin{bmatrix}
2 \\
0
\end{bmatrix}
=2e_1
$$

입니다.

결과는 가로 방향 그대로입니다. 길이만 $2$배가 되었습니다.

이번에는 세로 방향 벡터를 봅시다.

$$
e_2=
\begin{bmatrix}
0 \\
1
\end{bmatrix}
$$

그러면

$$
Ae_2=
\begin{bmatrix}
0 \\
3
\end{bmatrix}
=3e_2
$$

입니다.

세로 방향도 그대로이고 길이만 $3$배가 되었습니다.

# 7. 고유벡터와 고유값

행렬 $A$를 곱했는데 방향이 바뀌지 않는 벡터가 있을 수 있습니다.

그런 벡터를 고유벡터라고 합니다.

고유벡터는 영벡터가 아니어야 합니다.

고유벡터가 몇 배가 되었는지를 나타내는 수를 고유값이라고 합니다.

이 관계를 식으로 쓰면

$$
Av=\lambda v
$$

입니다.

여기서 $v$는 고유벡터이고, $\lambda$는 고유값입니다.

이 식은 이렇게 읽습니다.

> $A$가 $v$를 변환했더니, 방향은 그대로이고 크기만 $\lambda$배가 되었다.

# 8. 고유벡터는 왜 영벡터가 아니어야 하는가

영벡터

$$
\begin{bmatrix}
0 \\
0
\end{bmatrix}
$$

는 어떤 행렬을 곱해도 보통 영벡터로 갑니다.

하지만 영벡터는 방향이 없습니다.

고유벡터는 방향이 변하지 않는 벡터를 찾는 개념입니다.

방향이 없는 영벡터를 고유벡터로 허용하면 모든 것이 의미 없어집니다.

그래서 고유벡터는 반드시 영벡터가 아니어야 합니다.

# 9. 고유값을 직접 확인해 보자

행렬

$$
A=
\begin{bmatrix}
4 & 0 \\
0 & 2
\end{bmatrix}
$$

를 봅시다.

벡터

$$
v=
\begin{bmatrix}
1 \\
0
\end{bmatrix}
$$

에 곱하면

$$
Av=
\begin{bmatrix}
4 \\
0
\end{bmatrix}
=4
\begin{bmatrix}
1 \\
0
\end{bmatrix}
=4v
$$

입니다.

따라서 $v$는 고유벡터이고, 고유값은 $4$입니다.

벡터

$$
w=
\begin{bmatrix}
0 \\
1
\end{bmatrix}
$$

에 곱하면

$$
Aw=
\begin{bmatrix}
0 \\
2
\end{bmatrix}
=2w
$$

입니다.

따라서 $w$도 고유벡터이고, 고유값은 $2$입니다.

# 10. 고유벡터가 아닌 경우

같은 행렬

$$
A=
\begin{bmatrix}
4 & 0 \\
0 & 2
\end{bmatrix}
$$

에 벡터

$$
u=
\begin{bmatrix}
1 \\
1
\end{bmatrix}
$$

를 곱해 봅시다.

$$
Au=
\begin{bmatrix}
4 \\
2
\end{bmatrix}
$$

입니다.

이 결과는

$$
\begin{bmatrix}
1 \\
1
\end{bmatrix}
$$

의 몇 배가 아닙니다.

$u$의 방향은 대각선 방향인데, $Au$는 다른 방향입니다.

따라서 $u$는 고유벡터가 아닙니다.

# 11. 고유값은 특성방정식으로 찾는다

고유값은

$$
Av=\lambda v
$$

에서 나옵니다.

오른쪽을 왼쪽으로 옮기면

$$
Av-\lambda v=0
$$

입니다.

단위행렬 $I$를 이용하면

$$
\lambda v=\lambda Iv
$$

이므로

$$
(A-\lambda I)v=0
$$

입니다.

영벡터가 아닌 $v$가 존재하려면 행렬 $A-\lambda I$가 공간을 눌러 납작하게 만드는 상황이어야 합니다.

이 조건은

$$
\det(A-\lambda I)=0
$$

으로 씁니다.

이 식을 특성방정식이라고 합니다.

# 12. 2차 대각행렬의 고유값 찾기

행렬

$$
A=
\begin{bmatrix}
4 & 0 \\
0 & 2
\end{bmatrix}
$$

를 봅시다.

$$
A-\lambda I=
\begin{bmatrix}
4-\lambda & 0 \\
0 & 2-\lambda
\end{bmatrix}
$$

입니다.

행렬식은

$$
\det(A-\lambda I)=(4-\lambda)(2-\lambda)
$$

입니다.

특성방정식은

$$
(4-\lambda)(2-\lambda)=0
$$

입니다.

따라서

$$
\lambda=4
$$

또는

$$
\lambda=2
$$

입니다.

# 13. 대각화는 좋은 기준으로 변환을 쉽게 읽는 것이다

어떤 행렬은 처음 기준에서는 복잡하게 보입니다.

하지만 고유벡터 방향을 기준으로 잡으면, 변환이 단순해질 수 있습니다.

고유벡터 방향에서는 행렬이 방향을 섞지 않고 몇 배만 합니다.

그래서 고유벡터들을 기준으로 잡으면 행렬을 축별 늘림과 줄임으로 읽을 수 있습니다.

이 생각이 대각화입니다.

# 14. 왜 AI 수학에서 고유값이 중요한가

행렬은 데이터를 바꾸는 규칙으로 자주 등장합니다.

고유값은 그 규칙이 어떤 방향을 얼마나 키우거나 줄이는지 알려 줍니다.

예를 들어 어떤 방향의 고유값이 크면, 그 방향 성분은 변환 뒤 크게 남습니다.

어떤 방향의 고유값이 작으면, 그 방향 성분은 작아집니다.

그래서 PCA, 안정성 분석, 그래프 분석, 신경망의 행렬 계산에서 고유값과 고유벡터가 중요합니다.

# 15. 예제 1: 고유벡터 확인하기

문제: 다음 행렬과 벡터에 대해 $v$가 고유벡터인지 확인하시오.

$$
A=
\begin{bmatrix}
3 & 0 \\
0 & 5
\end{bmatrix},
\qquad
v=
\begin{bmatrix}
1 \\
0
\end{bmatrix}
$$

풀이:

$$
Av=
\begin{bmatrix}
3 \\
0
\end{bmatrix}
=3
\begin{bmatrix}
1 \\
0
\end{bmatrix}
=3v
$$

따라서 $v$는 고유벡터이고 고유값은 $3$입니다.

# 16. 예제 2: 고유벡터가 아닌 경우

문제: 다음 행렬과 벡터에 대해 $u$가 고유벡터인지 확인하시오.

$$
A=
\begin{bmatrix}
3 & 0 \\
0 & 5
\end{bmatrix},
\qquad
u=
\begin{bmatrix}
1 \\
1
\end{bmatrix}
$$

풀이:

$$
Au=
\begin{bmatrix}
3 \\
5
\end{bmatrix}
$$

입니다.

이 벡터는

$$
\begin{bmatrix}
1 \\
1
\end{bmatrix}
$$

의 몇 배가 아닙니다.

따라서 $u$는 고유벡터가 아닙니다.

# 17. 예제 3: 고유값 찾기

문제: 다음 행렬의 고유값을 찾으시오.

$$
A=
\begin{bmatrix}
6 & 0 \\
0 & -1
\end{bmatrix}
$$

풀이:

대각행렬에서는 대각선 위의 값이 고유값입니다.

따라서 고유값은

$$
6,\qquad -1
$$

입니다.

# 18. 한 줄씩 다시 요약하기

- 변환은 벡터를 다른 벡터로 보내는 규칙이다.
- 행렬은 벡터를 변환하는 규칙으로 볼 수 있다.
- 선형변환은 더하기와 스칼라배 구조를 보존한다.
- 고유벡터는 변환 뒤에도 방향이 바뀌지 않는 영벡터가 아닌 벡터다.
- 고유값은 고유벡터가 몇 배가 되는지를 나타낸다.
- 고유벡터와 고유값의 관계는 $Av=\lambda v$이다.
- 특성방정식은 $\det(A-\lambda I)=0$이다.
- 대각화는 고유벡터 방향을 기준으로 변환을 쉽게 읽는 방법이다.

# 19. 스스로 점검

1. 행렬을 변환으로 볼 수 있는 이유를 설명할 수 있는가?
2. $Av=\lambda v$를 말로 풀어 설명할 수 있는가?
3. 고유벡터가 왜 영벡터가 아니어야 하는지 설명할 수 있는가?
4. 대각행렬의 고유값을 찾을 수 있는가?
5. 고유값이 어떤 방향이 얼마나 커지는지 알려 준다는 말을 설명할 수 있는가?
