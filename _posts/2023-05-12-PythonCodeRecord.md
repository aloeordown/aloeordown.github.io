---
layout: mypost
title: PythonCodeRecord
categories: [记录]
---

1. Hanota Problem

   ```python
   def hanota(A: list[int], B:List[int], C:List[int]):
       n=len(A)
       if n==1:
           C.append(A.pop())
       else:
           hanota(A, C, B)
           C.append(A.pop())
           hanota(B, A, C)        
   ```

   A,B,C表示三个柱子，初始状态为A中有降序的数字，代表大小的盘子。

   思路：递归问题，当盘子数量大于1时，归纳为三个步骤：

   - 把n-1个盘子从A移到B

   - 把最后一个盘子从A移到C

   - 把B上的盘子移到C

2. 用切片实现去除字符串首尾空格：

   ```python
   def trim(s):
     if s[:1] == ' ':
       return trim(s[1:])
     if s[-1:] == ' ':
       return trim(s[:-1])
     return s
   ```

   

3. 暂定