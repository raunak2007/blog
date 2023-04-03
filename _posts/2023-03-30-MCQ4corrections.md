---
title: MCQ 4 Blog and Corrections
description: MCQ 4 Blog and Corrections (March 30th, 2023)
toc: true
comments: true
layout: post
permalink: /week28/MCQ4
categories: [week 28]
---


# MCQ
## Results

I scored a 45/50, or 90%

### Proof of Completion

![proof](https://user-images.githubusercontent.com/111464932/228932312-f239e6c1-3b50-429d-8542-0630ffcc7430.png)


## Corrections

### Q1

![Q1](https://user-images.githubusercontent.com/111464932/228933206-260b4566-e051-4497-a29d-baece1972065.png)

My answer: (B) 70 seconds

Correct answer: (C) 80 seconds

### Q3

[Q3](https://user-images.githubusercontent.com/111464932/228933706-2c58ae6d-f46a-481c-934c-fdb2fce963c4.png)

My answer: (D) 4

Correct answer: (C) 3

> My answer is incorrect. While removing four links could isolate computer F from computer E, it is not the minimum number required to accomplish this. We could isolate computer F completely by only removing 3 links.

> Any line between two computers represents a way for them to communicate with each other, and a communication between two computers can go through other computers. If the links from F to G, from F to A, and from F to E were broken, it would not be possible for computers E and F to communicate.

### Q34

![Q34](https://user-images.githubusercontent.com/111464932/228934474-a6103e2b-7457-44a3-9ce1-f5f4294c3a5c.png)

My answer: (C) Show that for one instance of the problem, a heuristic is needed to write an algorithm that is capable of providing a correct yes-or-no answer.

Correct answer: (B) Show that for one instance of the problem, no algorithm can be written that is capable of providing a correct yes-or-no answer.

> This statement does not provide enough information to conclude that the problem is undecidable. This states that a heuristic is used for one instance of the problem. If it could be shown that an algorithm can be constructed that is always capable of providing a correct yes-or-no answer for all other instances of this problem, then this problem would be decidable.

> A decidable problem is one for which an algorithm can be constructed to produce a correct output for all inputs. If, for one instance of the problem, this is not possible, then this problem cannot be decidable. Therefore, it must be undecidable.

### Q37

![Q37](https://user-images.githubusercontent.com/111464932/228935236-6ff255e9-abc3-4e48-9113-2fb8b762d080.png)

My answer: (D) The algorithm runs in an unreasonable amount of time because it will use approximately *n^2* steps to draw *n* shapes.

Correct answer: (B) The algorithm runs in a reasonable amount of time because it will use approximately *n^2* steps to draw *n* shapes.

> It is correct that as *n* increases, the number of steps is approximately equal to *n^2*. However, that means the algorithm runs in a reasonable amount of time.

> As *n* increases, the number of steps is approximately equal to *n^2*, which would make the algorithm polynomial. An algorithm with an efficiency that approximates *n^2* is said to run in a reasonable amount of time.

### Q49

![Q49](https://user-images.githubusercontent.com/111464932/228936271-494d29c2-8e95-4211-9cbd-11ea81178146.png)

My answer: (C)

Correct answer: (A)

> This code segment traverses the list beginning with the second element, so it is correctly comparing only the student scores to the maximum possible score. However, the code segment will fail to check the last element in the list. When index is equal to the length of the list, the loop will terminate without comparing the last student score in the list to the maximum possible score.

> The correct code segment traverses the list beginning with the second element, so it is correctly comparing only student scores to the maximum possible score, which is found by accessing scores[1]. The variable found will only be set to true when a student’s score equals the maximum possible score. The code also sets the number of iterations to LENGTH(scores) - 1 to reflect that the first list element (maximum score) is skipped.
