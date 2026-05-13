---
title: "07. 벡터공간과 기저"
source_kind: page
source_path: ssot/pages/31ee313f58b980d68c5ad8ed9d5aeff8__SenseCore AI LAB, AI융합학부/children/lecture/32be313f58b980078dbbeed4f006f95b__Lecture/children/math/32be313f58b981e7b26fea2d45e6fa7f__AI를 위한 수학/children/32be313f58b981dfaa1ef692510e6dfa__02. 식과 방정식의 언어/children/32ce313f58b981c79bfff023a1b3ac9a__7. 벡터공간과 기저
notion_id: 32ce313f58b981c79bfff023a1b3ac9a
notion_url: https://www.notion.so/32ce313f58b981c79bfff023a1b3ac9a
parent_notion_id: 32be313f58b981dfaa1ef692510e6dfa
---
# 7강. 벡터공간과 기저

이 강의의 목표는 아래 벡터를 보고, 이것이 무엇을 뜻하는지 말할 수 있게 되는 것입니다.

$$
\begin{bmatrix}
3 \\
2
\end{bmatrix}
$$

이 벡터는 오른쪽으로 $3$, 위로 $2$ 가는 화살표로 볼 수 있습니다. 벡터공간과 기저는 이런 화살표들을 어떤 기준으로 설명할지 정하는 언어입니다.

# 1. 먼저 오늘 쓸 말을 정리하자

| 말 | 뜻 |
|---|---|
| 벡터 | 여러 숫자를 순서 있게 묶은 것 |
| 성분 | 벡터 안의 각각의 숫자 |
| 스칼라 | 벡터를 몇 배 할 때 쓰는 보통의 수 |
| 벡터 덧셈 | 같은 위치의 성분끼리 더하는 계산 |
| 스칼라배 | 벡터의 모든 성분에 같은 수를 곱하는 계산 |
| 선형결합 | 벡터들을 몇 배씩 해서 더한 것 |
| 기저 | 공간을 만들기 위한 기준 벡터 묶음 |
| 차원 | 필요한 기준 방향의 개수 |
| 좌표 | 기준 벡터를 얼마씩 썼는지 적은 숫자 |

# 2. 벡터는 숫자 묶음이다

벡터

$$
v=
\begin{bmatrix}
3 \\
2
\end{bmatrix}
$$

를 봅시다.

이 벡터에는 숫자 두 개가 있습니다.

- 첫 번째 성분은 $3$입니다.
- 두 번째 성분은 $2$입니다.

2차원 평면에서는 첫 번째 성분을 가로 방향, 두 번째 성분을 세로 방향으로 읽을 수 있습니다.

따라서

$$
\begin{bmatrix}
3 \\
2
\end{bmatrix}
$$

는 오른쪽으로 $3$, 위로 $2$ 가는 화살표입니다.

# 3. 벡터는 위치가 아니라 이동으로 볼 수 있다

점 $(3,2)$와 벡터

$$
\begin{bmatrix}
3 \\
2
\end{bmatrix}
$$

는 비슷해 보입니다.

점은 위치를 말합니다.

벡터는 이동을 말합니다.

즉 벡터는 이렇게 읽을 수 있습니다.

> 어디서 시작하든 오른쪽으로 $3$, 위로 $2$ 이동한다.

그래서 벡터는 방향과 크기를 가진 화살표로 생각할 수 있습니다.

# 4. 벡터 덧셈은 성분끼리 더한다

두 벡터가 있습니다.

$$
u=
\begin{bmatrix}
1 \\
2
\end{bmatrix},
\qquad
v=
\begin{bmatrix}
3 \\
4
\end{bmatrix}
$$

두 벡터를 더하면 같은 위치의 성분끼리 더합니다.

$$
u+v=
\begin{bmatrix}
1+3 \\
2+4
\end{bmatrix}
=
\begin{bmatrix}
4 \\
6
\end{bmatrix}
$$

벡터 덧셈은 이동을 이어 붙이는 것과 같습니다.

먼저 오른쪽으로 $1$, 위로 $2$ 가고, 그다음 오른쪽으로 $3$, 위로 $4$ 가면 전체는 오른쪽으로 $4$, 위로 $6$ 간 것입니다.

# 5. 스칼라배는 벡터를 늘리거나 줄인다

스칼라는 보통의 숫자입니다.

벡터

$$
v=
\begin{bmatrix}
3 \\
2
\end{bmatrix}
$$

에 $2$를 곱해 봅시다.

$$
2v=
2
\begin{bmatrix}
3 \\
2
\end{bmatrix}
=
\begin{bmatrix}
6 \\
4
\end{bmatrix}
$$

모든 성분에 $2$를 곱했습니다.

방향은 같고 길이는 더 길어졌습니다.

이번에는 $-1$을 곱해 봅시다.

$$
-v=
-1
\begin{bmatrix}
3 \\
2
\end{bmatrix}
=
\begin{bmatrix}
-3 \\
-2
\end{bmatrix}
$$

방향이 반대로 바뀝니다.

# 6. 선형결합은 벡터들을 섞어서 만드는 것이다

두 벡터

$$
u=
\begin{bmatrix}
1 \\
0
\end{bmatrix},
\qquad
v=
\begin{bmatrix}
0 \\
1
\end{bmatrix}
$$

가 있다고 합시다.

이 벡터들을 몇 배씩 해서 더해 봅시다.

$$
3u+2v
$$

계산하면

$$
3
\begin{bmatrix}
1 \\
0
\end{bmatrix}
+2
\begin{bmatrix}
0 \\
1
\end{bmatrix}
=
\begin{bmatrix}
3 \\
0
\end{bmatrix}
+
\begin{bmatrix}
0 \\
2
\end{bmatrix}
=
\begin{bmatrix}
3 \\
2
\end{bmatrix}
$$

입니다.

이처럼 벡터들을 스칼라배한 뒤 더해서 새 벡터를 만드는 것을 선형결합이라고 합니다.

# 7. 기준 벡터로 평면의 모든 벡터를 만들 수 있다

두 벡터

$$
e_1=
\begin{bmatrix}
1 \\
0
\end{bmatrix},
\qquad
e_2=
\begin{bmatrix}
0 \\
1
\end{bmatrix}
$$

를 봅시다.

$e_1$은 오른쪽 방향 기준 벡터입니다.

$e_2$는 위쪽 방향 기준 벡터입니다.

평면의 벡터

$$
\begin{bmatrix}
3 \\
2
\end{bmatrix}
$$

는 다음처럼 만들 수 있습니다.

$$
\begin{bmatrix}
3 \\
2
\end{bmatrix}
=3e_1+2e_2
$$

즉 오른쪽 기준 벡터를 $3$개, 위쪽 기준 벡터를 $2$개 쓴 것입니다.

# 8. 기저는 공간을 만드는 최소 기준 벡터 묶음이다

기저는 공간의 모든 벡터를 만들 수 있는 기준 벡터 묶음입니다.

2차원 평면에서는 보통

$$
e_1=
\begin{bmatrix}
1 \\
0
\end{bmatrix},
\qquad
e_2=
\begin{bmatrix}
0 \\
1
\end{bmatrix}
$$

를 기저로 씁니다.

이 두 벡터만 있으면 평면의 모든 벡터를 만들 수 있습니다.

예를 들어

$$
\begin{bmatrix}
-4 \\
7
\end{bmatrix}
=-4e_1+7e_2
$$

입니다.

# 9. 독립인 기준이 필요하다

기저가 되려면 기준 벡터들이 서로 같은 방향만 보고 있으면 안 됩니다.

예를 들어

$$
\begin{bmatrix}
1 \\
0
\end{bmatrix}
$$

와

$$
\begin{bmatrix}
2 \\
0
\end{bmatrix}
$$

는 둘 다 가로 방향입니다.

이 두 벡터를 아무리 섞어도 위쪽으로 움직이는 벡터를 만들 수 없습니다.

예를 들어

$$
\begin{bmatrix}
0 \\
1
\end{bmatrix}
$$

는 만들 수 없습니다.

그래서 기저 벡터들은 서로 새로운 방향을 제공해야 합니다. 이것을 선형독립이라고 부릅니다.

# 10. 차원은 필요한 기준 방향의 개수다

수직선 위에서는 한 방향만 있으면 충분합니다.

예를 들어 오른쪽 방향 기준 하나만 있으면 됩니다.

그래서 수직선은 1차원입니다.

평면에서는 오른쪽 방향과 위쪽 방향이 필요합니다.

그래서 평면은 2차원입니다.

공간에서는 오른쪽, 앞쪽, 위쪽처럼 세 방향이 필요합니다.

그래서 우리가 사는 공간은 보통 3차원으로 생각합니다.

차원은 어려운 말이 아니라, 위치나 이동을 설명하는 데 필요한 독립적인 기준 방향의 개수입니다.

# 11. 좌표는 기준 벡터를 얼마씩 썼는지 적은 것이다

벡터

$$
\begin{bmatrix}
3 \\
2
\end{bmatrix}
$$

는 표준기저

$$
e_1=
\begin{bmatrix}
1 \\
0
\end{bmatrix},
\qquad
e_2=
\begin{bmatrix}
0 \\
1
\end{bmatrix}
$$

에 대해

$$
3e_1+2e_2
$$

로 만들어집니다.

따라서 좌표 $(3,2)$는 기준 벡터 $e_1$을 $3$만큼, $e_2$를 $2$만큼 썼다는 뜻입니다.

# 12. 벡터공간은 벡터들이 살고 계산되는 세계다

벡터공간은 벡터들을 더하고, 숫자를 곱해도 다시 그 안에 머무르는 공간입니다.

예를 들어 2차원 벡터들의 모임을 생각해 봅시다.

$$
\begin{bmatrix}
a \\
b
\end{bmatrix}
$$

모양의 모든 벡터가 들어 있습니다.

이 안의 두 벡터를 더하면 다시 2차원 벡터입니다.

이 안의 벡터에 숫자를 곱해도 다시 2차원 벡터입니다.

그래서 2차원 벡터 전체는 벡터공간입니다.

# 13. 예제 1: 벡터 덧셈

문제: 다음 벡터를 더하시오.

$$
\begin{bmatrix}
2 \\
-1
\end{bmatrix}
+
\begin{bmatrix}
3 \\
5
\end{bmatrix}
$$

풀이:

성분끼리 더합니다.

$$
\begin{bmatrix}
2+3 \\
-1+5
\end{bmatrix}
=
\begin{bmatrix}
5 \\
4
\end{bmatrix}
$$

# 14. 예제 2: 선형결합 계산하기

문제: 다음 값을 구하시오.

$$
2
\begin{bmatrix}
1 \\
2
\end{bmatrix}
-3
\begin{bmatrix}
0 \\
1
\end{bmatrix}
$$

풀이:

$$
2
\begin{bmatrix}
1 \\
2
\end{bmatrix}
=
\begin{bmatrix}
2 \\
4
\end{bmatrix}
$$

이고

$$
3
\begin{bmatrix}
0 \\
1
\end{bmatrix}
=
\begin{bmatrix}
0 \\
3
\end{bmatrix}
$$

입니다.

따라서

$$
\begin{bmatrix}
2 \\
4
\end{bmatrix}
-
\begin{bmatrix}
0 \\
3
\end{bmatrix}
=
\begin{bmatrix}
2 \\
1
\end{bmatrix}
$$

입니다.

# 15. 예제 3: 기저로 표현하기

문제: 표준기저 $e_1$, $e_2$를 이용해 다음 벡터를 표현하시오.

$$
\begin{bmatrix}
-2 \\
6
\end{bmatrix}
$$

풀이:

표준기저는

$$
e_1=
\begin{bmatrix}
1 \\
0
\end{bmatrix},
\qquad
e_2=
\begin{bmatrix}
0 \\
1
\end{bmatrix}
$$

입니다.

따라서

$$
\begin{bmatrix}
-2 \\
6
\end{bmatrix}
=-2e_1+6e_2
$$

입니다.

# 16. 한 줄씩 다시 요약하기

- 벡터는 여러 숫자를 순서 있게 묶은 것이다.
- 2차원 벡터는 가로 성분과 세로 성분으로 읽을 수 있다.
- 벡터 덧셈은 같은 위치의 성분끼리 더한다.
- 스칼라배는 모든 성분에 같은 수를 곱한다.
- 선형결합은 벡터들을 몇 배씩 해서 더한 것이다.
- 기저는 공간을 만드는 기준 벡터 묶음이다.
- 기저 벡터들은 서로 새로운 방향을 제공해야 한다.
- 차원은 필요한 독립적인 기준 방향의 개수다.
- 좌표는 기준 벡터를 얼마씩 썼는지 적은 것이다.

# 17. 스스로 점검

1. $\begin{bmatrix}4\\-1\end{bmatrix}$를 말로 설명할 수 있는가?
2. 두 벡터를 성분끼리 더할 수 있는가?
3. 스칼라배가 벡터를 어떻게 바꾸는지 설명할 수 있는가?
4. $3e_1+5e_2$가 어떤 벡터인지 말할 수 있는가?
5. 평면이 왜 2차원인지 설명할 수 있는가?
