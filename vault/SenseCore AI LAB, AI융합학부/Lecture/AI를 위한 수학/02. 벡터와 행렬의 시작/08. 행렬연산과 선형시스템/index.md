---
title: "08. 행렬연산과 선형시스템"
source_kind: page
source_path: ssot/pages/31ee313f58b980d68c5ad8ed9d5aeff8__SenseCore AI LAB, AI융합학부/children/lecture/32be313f58b980078dbbeed4f006f95b__Lecture/children/math/32be313f58b981e7b26fea2d45e6fa7f__AI를 위한 수학/children/32be313f58b981dfaa1ef692510e6dfa__02. 식과 방정식의 언어/children/32ce313f58b981ff91c1fb25407aebb8__8. 행렬연산과 선형시스템
notion_id: 32ce313f58b981ff91c1fb25407aebb8
notion_url: https://www.notion.so/32ce313f58b981ff91c1fb25407aebb8
parent_notion_id: 32be313f58b981dfaa1ef692510e6dfa
---
# 8강. 행렬연산과 선형시스템

이 강의의 목표는 아래 식을 보고, 행렬이 벡터를 어떻게 계산하는지 설명할 수 있게 되는 것입니다.

$$
Ax=b
$$

이 식은 행렬 $A$와 벡터 $x$를 곱한 결과가 벡터 $b$가 된다는 뜻입니다.

# 1. 먼저 오늘 쓸 말을 정리하자

| 말 | 뜻 |
|---|---|
| 행렬 | 숫자를 직사각형 표처럼 배열한 것 |
| 행 | 행렬의 가로줄 |
| 열 | 행렬의 세로줄 |
| 성분 | 행렬 안의 각각의 숫자 |
| 행렬곱 | 행과 열을 맞추어 계산하는 곱셈 |
| 단위행렬 | 곱해도 대상을 바꾸지 않는 행렬 |
| 역행렬 | 행렬의 작용을 되돌리는 행렬 |
| 선형시스템 | 여러 개의 일차방정식을 한꺼번에 묶은 것 |

# 2. 행렬은 숫자 표다

다음 행렬을 봅시다.

$$
A=
\begin{bmatrix}
1 & 2 \\
3 & 4
\end{bmatrix}
$$

이 행렬에는 가로줄이 두 개, 세로줄이 두 개 있습니다.

첫 번째 행은

$$
\begin{bmatrix}
1 & 2
\end{bmatrix}
$$

입니다.

두 번째 행은

$$
\begin{bmatrix}
3 & 4
\end{bmatrix}
$$

입니다.

첫 번째 열은

$$
\begin{bmatrix}
1 \\
3
\end{bmatrix}
$$

입니다.

두 번째 열은

$$
\begin{bmatrix}
2 \\
4
\end{bmatrix}
$$

입니다.

# 3. 행렬의 크기 읽기

행렬의 크기는 행의 개수와 열의 개수로 말합니다.

$$
\begin{bmatrix}
1 & 2 \\
3 & 4
\end{bmatrix}
$$

은 행이 $2$개, 열이 $2$개입니다.

그래서 $2\times 2$ 행렬이라고 합니다.

다음 행렬은

$$
\begin{bmatrix}
1 & 2 & 3 \\
4 & 5 & 6
\end{bmatrix}
$$

행이 $2$개, 열이 $3$개입니다.

그래서 $2\times 3$ 행렬입니다.

# 4. 행렬 덧셈은 같은 자리끼리 더한다

두 행렬이 있습니다.

$$
A=
\begin{bmatrix}
1 & 2 \\
3 & 4
\end{bmatrix},
\qquad
B=
\begin{bmatrix}
5 & 6 \\
7 & 8
\end{bmatrix}
$$

두 행렬을 더하면 같은 위치의 숫자끼리 더합니다.

$$
A+B=
\begin{bmatrix}
1+5 & 2+6 \\
3+7 & 4+8
\end{bmatrix}
=
\begin{bmatrix}
6 & 8 \\
10 & 12
\end{bmatrix}
$$

행렬 덧셈을 하려면 두 행렬의 크기가 같아야 합니다.

# 5. 행렬의 스칼라배는 모든 성분에 곱한다

행렬

$$
A=
\begin{bmatrix}
1 & 2 \\
3 & 4
\end{bmatrix}
$$

에 $2$를 곱하면 모든 성분에 $2$를 곱합니다.

$$
2A=
\begin{bmatrix}
2 & 4 \\
6 & 8
\end{bmatrix}
$$

# 6. 행렬과 벡터의 곱은 가중합이다

행렬

$$
A=
\begin{bmatrix}
1 & 2 \\
3 & 4
\end{bmatrix}
$$

와 벡터

$$
x=
\begin{bmatrix}
5 \\
6
\end{bmatrix}
$$

를 곱해 봅시다.

$$
Ax=
\begin{bmatrix}
1 & 2 \\
3 & 4
\end{bmatrix}
\begin{bmatrix}
5 \\
6
\end{bmatrix}
$$

첫 번째 결과 성분은 첫 번째 행과 벡터를 맞추어 계산합니다.

$$
1\cdot 5+2\cdot 6=5+12=17
$$

두 번째 결과 성분은 두 번째 행과 벡터를 맞추어 계산합니다.

$$
3\cdot 5+4\cdot 6=15+24=39
$$

따라서

$$
Ax=
\begin{bmatrix}
17 \\
39
\end{bmatrix}
$$

입니다.

# 7. 행렬곱은 행과 열을 맞추어 계산한다

이번에는 행렬끼리 곱해 봅시다.

$$
A=
\begin{bmatrix}
1 & 2 \\
3 & 4
\end{bmatrix},
\qquad
B=
\begin{bmatrix}
5 & 6 \\
7 & 8
\end{bmatrix}
$$

$AB$의 첫 번째 행, 첫 번째 열 성분은 $A$의 첫 번째 행과 $B$의 첫 번째 열을 맞추어 계산합니다.

$$
1\cdot 5+2\cdot 7=19
$$

첫 번째 행, 두 번째 열 성분은 $A$의 첫 번째 행과 $B$의 두 번째 열을 맞춥니다.

$$
1\cdot 6+2\cdot 8=22
$$

두 번째 행도 같은 방식으로 계산합니다.

$$
3\cdot 5+4\cdot 7=43
$$

$$
3\cdot 6+4\cdot 8=50
$$

따라서

$$
AB=
\begin{bmatrix}
19 & 22 \\
43 & 50
\end{bmatrix}
$$

입니다.

# 8. 행렬곱은 순서를 바꾸면 달라질 수 있다

숫자는 보통

$$
2\cdot 3=3\cdot 2
$$

입니다.

하지만 행렬은 일반적으로

$$
AB\neq BA
$$

입니다.

즉 행렬곱에서는 순서가 중요합니다.

이것은 행렬이 단순한 숫자가 아니라, 계산 규칙이나 변환을 나타내기 때문입니다.

# 9. 단위행렬은 곱해도 바꾸지 않는 행렬이다

2차원 단위행렬은

$$
I=
\begin{bmatrix}
1 & 0 \\
0 & 1
\end{bmatrix}
$$

입니다.

벡터

$$
x=
\begin{bmatrix}
5 \\
6
\end{bmatrix}
$$

에 곱해 봅시다.

$$
Ix=
\begin{bmatrix}
1 & 0 \\
0 & 1
\end{bmatrix}
\begin{bmatrix}
5 \\
6
\end{bmatrix}
=
\begin{bmatrix}
5 \\
6
\end{bmatrix}
$$

결과가 그대로입니다.

단위행렬은 숫자 $1$과 비슷한 역할을 합니다.

# 10. 역행렬은 되돌리는 행렬이다

숫자에서 $2$를 곱했다면 되돌리려면 $\frac{1}{2}$를 곱합니다.

행렬에서도 어떤 행렬 $A$를 곱한 일을 되돌리는 행렬이 있으면 그것을 역행렬이라고 합니다.

역행렬은

$$
A^{-1}
$$

라고 씁니다.

역행렬이 존재하면

$$
A^{-1}A=I
$$

입니다.

즉 $A$를 곱한 뒤 $A^{-1}$을 곱하면 원래대로 돌아갑니다.

# 11. 선형시스템은 여러 방정식을 한꺼번에 묶은 것이다

다음 연립방정식을 봅시다.

$$
\begin{aligned}
x+2y&=5 \\
3x+4y&=11
\end{aligned}
$$

이것을 행렬로 쓸 수 있습니다.

$$
\begin{bmatrix}
1 & 2 \\
3 & 4
\end{bmatrix}
\begin{bmatrix}
x \\
y
\end{bmatrix}
=
\begin{bmatrix}
5 \\
11
\end{bmatrix}
$$

짧게 쓰면

$$
Ax=b
$$

입니다.

여기서

$$
A=
\begin{bmatrix}
1 & 2 \\
3 & 4
\end{bmatrix},
\qquad
x=
\begin{bmatrix}
x \\
y
\end{bmatrix},
\qquad
b=
\begin{bmatrix}
5 \\
11
\end{bmatrix}
$$

입니다.

# 12. 역행렬이 있으면 해를 구할 수 있다

선형시스템

$$
Ax=b
$$

에서 $A$의 역행렬이 있으면 양쪽에 $A^{-1}$을 곱할 수 있습니다.

$$
A^{-1}Ax=A^{-1}b
$$

왼쪽은

$$
Ix=x
$$

가 됩니다.

그래서

$$
x=A^{-1}b
$$

입니다.

이 식은 행렬 방정식을 푸는 기본 형태입니다.

# 13. 예제 1: 행렬과 벡터 곱하기

문제: 다음 값을 구하시오.

$$
\begin{bmatrix}
2 & 1 \\
0 & 3
\end{bmatrix}
\begin{bmatrix}
4 \\
5
\end{bmatrix}
$$

풀이:

첫 번째 성분은

$$
2\cdot 4+1\cdot 5=13
$$

입니다.

두 번째 성분은

$$
0\cdot 4+3\cdot 5=15
$$

입니다.

따라서

$$
\begin{bmatrix}
13 \\
15
\end{bmatrix}
$$

입니다.

# 14. 예제 2: 연립방정식을 행렬로 쓰기

문제: 다음 연립방정식을 행렬식으로 쓰시오.

$$
\begin{aligned}
2x+y&=7 \\
x-3y&=4
\end{aligned}
$$

풀이:

계수만 모으면

$$
\begin{bmatrix}
2 & 1 \\
1 & -3
\end{bmatrix}
$$

입니다.

미지수는

$$
\begin{bmatrix}
x \\
y
\end{bmatrix}
$$

입니다.

오른쪽 값은

$$
\begin{bmatrix}
7 \\
4
\end{bmatrix}
$$

입니다.

따라서

$$
\begin{bmatrix}
2 & 1 \\
1 & -3
\end{bmatrix}
\begin{bmatrix}
x \\
y
\end{bmatrix}
=
\begin{bmatrix}
7 \\
4
\end{bmatrix}
$$

입니다.

# 15. 한 줄씩 다시 요약하기

- 행렬은 숫자를 행과 열로 배열한 표다.
- 행은 가로줄이고 열은 세로줄이다.
- 행렬 덧셈은 같은 자리끼리 더한다.
- 행렬의 스칼라배는 모든 성분에 같은 수를 곱한다.
- 행렬과 벡터의 곱은 행과 벡터를 맞추어 계산한다.
- 행렬곱은 행과 열을 맞추어 계산한다.
- 행렬곱은 순서가 바뀌면 결과가 달라질 수 있다.
- 단위행렬은 곱해도 대상을 바꾸지 않는다.
- 역행렬은 행렬의 작용을 되돌린다.
- 여러 일차방정식은 $Ax=b$로 묶을 수 있다.

# 16. 스스로 점검

1. $2\times 3$ 행렬이 어떤 모양인지 설명할 수 있는가?
2. 행렬 덧셈이 왜 같은 자리끼리 더하는 계산인지 말할 수 있는가?
3. 행렬과 벡터의 곱을 직접 계산할 수 있는가?
4. 단위행렬이 왜 숫자 $1$과 비슷한 역할인지 설명할 수 있는가?
5. 연립방정식을 $Ax=b$ 꼴로 바꿀 수 있는가?
