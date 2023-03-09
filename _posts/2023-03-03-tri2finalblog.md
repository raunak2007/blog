---
title: Trimester 2 Final Blog
description: Corrections and blog on trimester 2 final MCQ
toc: true
comments: true
layout: post
permalink: /week24/tri2finalblog
categories: [week 24]
---

# Final Exam
## Results
I scored a 46/50, or 92%. This is high enough to earn at least a .9/1 in the grade book.

![Proof of Final](https://awesomescreenshot.s3.amazonaws.com/image/2872977/37844028-42e757c067df0350988f37dfc604fa32.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAJSCJQ2NM3XLFPVKA%2F20230309%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20230309T220004Z&X-Amz-Expires=28800&X-Amz-SignedHeaders=host&X-Amz-Signature=6fd29039452f13cec7d306cbf5585090cef76fd80bda751e9992c9fa758673f9)

## Corrections

### Q2

Which of the following has the greatest potential for compromising a user’s personal privacy?


I answered: (B) B The Internet Protocol (IP) address of the user’s computer

Correct answer: (A) A group of cookies stored by the user’s Web browser

### Q5

A chain of retail stores uses software to manage telephone calls from customers. The system was recently upgraded. Customers interacted with the original system using their phone keypad. Customers interact with the upgraded system using their voice.

The upgraded system (but not the original system) stores all information from the calling session in a database for future reference. This includes the customer’s telephone number and any information provided by the customer (name, address, order number, credit card number, etc.).

The original system and the upgraded system are described in the following flowcharts. Each flowchart uses the following blocks.

![Q5](https://user-images.githubusercontent.com/111464932/222993386-8575ebce-27cc-48ff-bb97-dec329ec9145.png)

Of the following potential benefits, which is LEAST likely to be provided by the upgraded system?


I answered: (A) Human representatives will not be needed to respond to some inquiries.

Correct answer: (B) The company will be able to provide a human representative for any incoming call.

### Q36

A numeric test score is to be converted to a letter grade of A, B, or C according to the following rules: A score greater than 90 is considered an A; a score between 80 and 90, inclusive, is considered a B; and any other score is considered a C.

Which of the following code segments will assign the correct letter grade to `grade` based on the value of the variable `score` ?

![Q36](https://user-images.githubusercontent.com/111464932/222993598-d2c1aa07-b1db-42b1-810b-a7f2dd9692de.png)


I answered: (A) II only

Correct answer: (D) II and III only

### Q38

Consider the following code segment with an integer variable num.

    IF(num > 0)
    {
        DISPLAY("positive")
    }
    IF(num < 0)
    {
        DISPLAY("negative")
    }
    IF(num = 0)
    {
        DISPLAY("zero")
    }

Which of the following code segments is equivalent to the code segment above?

I answered: (A)

    IF(num < 0)
    {
        DISPLAY("negative")
    }
    ELSE
    {
        DISPLAY("positive")
    }
    IF(num = 0)
    {
        DISPLAY("zero")
    }


Correct answer: (B)

    IF(num < 0)
    {
        DISPLAY("negative")
    }
    ELSE
    {
        IF(num = 0)
        {
            DISPLAY("zero")
        }
        ELSE
        {
            DISPLAY("positive")
        }
    }


## Final Thoughts and Blogging

- Final exam wasn't too bad when working with classmates
- Most of it was pretty common sense to us
    - Digital security
    - Unethical uses of computer resources
    - Multifactor Authentication
- Other parts were just simple math and following directions
    - follow along with what a program is doing
    - Re-write a program with less complexity
    - Tell a robot what to do in order to move to a certain spot on a grid
