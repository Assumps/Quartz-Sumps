---
title: LeetCode Merge Sort Array
draft: false
tags:
---

# English
# Intuition

<!-- Describe your first thoughts on how to solve this problem. -->

##### To solve this problem i think in change the zero values in Array one to values on Array 2.


# Approach

<!-- Describe your approach to solving the problem. -->

##### In first case i create one For and define variables to count, var i for count the Array 1 and J to validate positions on Array 2.

##### After this i validate the zero inside Array 1, on next step i see in test case that if i have more zeros in Array 1 than Array 2 i will be a problem about index Out of Bounds, then validate if J is less than N, to avoid this problem.

  
# Complexity

- Time complexity: O((m+n)log(m+n))

<!-- Add your time complexity here, e.g. $$O(n)$$ -->
  

- Space complexity: O(m+n)

<!-- Add your space complexity here, e.g. $$O(n)$$ -->

---  
# Portuguese

# Intuição

<!-- Descreva seus primeiros pensamentos sobre como resolver este problema. -->

##### Para resolver este problema, penso em mudar os valores zero no Array um para valores no Array 2.


# Abordagem

<!-- Descreva sua abordagem para resolver o problema.  -->

##### INo primeiro caso, crio um For e defino variáveis ​​para contar, var i para contar o Array 1 e J para validar posições no Array 2.

##### Depois disso, valido o zero dentro do Array 1, na próxima etapa, vejo no caso de teste que se eu tiver mais zeros no Array 1 do que no Array 2, terei um problema sobre o índice Out of Bounds, então valido se J for menor que N, para evitar este problema.

  
# Complexidade

- Complexidade de tempo: O((m+n)log(m+n))

<!-- Adicione sua complexidade de tempo aqui, por exemplo. $$O(n)$$ -->

  
- Complexidade do espaço: O(m+n)

<!-- Adicione sua complexidade do espaço aqui, por exemplo $$O(n)$$ -->


# Code

```csharp []

public class Solution {

    public void Merge(int[] nums1, int m, int[] nums2, int n) {

        var counter = m + n;

        var j = 0;

  

        for(int i = 0; i < counter ; i++){

            if(nums1[i] == 0){            

                if(j < n){

                    nums1[i] = nums2[j];

                    j++;

                }

            }

        }

  

        Array.Sort(nums1);

    }

}

```