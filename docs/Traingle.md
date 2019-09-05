问题描述：给定一个三角形，找到一条从顶部到底部的路径，要求路径上的和值最小，每一步你只能往下一行的相邻位置走下去。

这题是典型的利用动态规划方式思考的问题，设f(i, j)是从第一行到第i行，第j个数字的最小和值，那么f(i, j)要么是从f(i-1, j-1)而来，要么是从f(i-1, j)而来，因此，最优子结构有：
f(i, j) = min(f(i-1, j-1), f(i-1, j)) + triangle[i][j]，通过这种方式，可以得到从第一行到第n行的所有点的最小和值，然后取第n行的最小值即可。

[代码](https://github.com/HCMY/InteletTree/blob/master/Leetcode/DP/Medium/Triangle.cc)
