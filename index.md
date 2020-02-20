## Welcome!

Read this page to join our group! Each week we read one textbook chapter and then discuss it on Tuesday. You can catch up quickly by reading this page and following the exercises. If you want to study the material more closely, please read any chapters you missed. Feel free to contact me, JLHerzberg, on slack with questions.

We are using this [textbook](https://d1b10bmlvqabco.cloudfront.net/attach/ighbo26t3ua52t/igp9099yy4v10/igz7vp4w5su9/OReilly_HandsOn_Programming_with_R_2014.pdf).

Other links: [FAQ](https://jlherzberg.github.io/RLearningGroup/faq.html)

### Chapter 0
You don't need to download R to participate in the weekly discussion. You do need to download R and RStudio to code on your own. Please watch this [video](https://www.youtube.com/watch?v=cX532N_XLIs) to download R and RStudio.

### Chapter 1
<details>
  <summary>1. Add ```6``` and ```10``` together with R.</summary>
  
    ```6+10```
</details>
<details>
  <summary>2. Set the object ```x``` equal to ```8```.</summary>
  
    ```x <- 8 or x = 8```
</details>
<details>
  <summary>3. Set the object die equal to the range of numbers ```1``` through ```6```.</summary>
  
    ```die <- 1:6```
</details>
<details>
  <summary>4. Compare die to the range numbers ```5``` through ```6```. </summary>
  
    ```die == 5:6```
</details>
<details>
  <summary>5. Compute the mean of ```5``` and ```8```.</summary>
  
    ```mean(8, 5)```
</details>
<details>
  <summary>6. Write a comment with ```#```.</summary>
  
    ```# i'm a comment!```
</details>
<details>
  <summary>7. Write a function that rolls two dice with the ```sample``` function and returns their sum.</summary>
  
    ```
    roll <- function() {
     die <- 1:6
     dice <- sample(die, size = 2, replace= TRUE)
     sum(dice)
    }
    ```
</details>
<details>
  <summary>8. Rewrite that function with an argument parameter for the number of dice to roll. </summary>
  
    ```
    roll <- function(num_dice=2) {
     die <- 1:6
     dice <- sample(die, size = num_dice, replace= TRUE)
     sum(dice)
    }
    ```
</details>

### Chapter 2
1. Install `ggplot`, which includes `qplot`.
2. Import `qplot`.
3. Plot a scatter plot.
4. Plot a histogram.
5. Explain how the `binwidth` argument works.
6. Use the `replicate` function to produce 10 rolls of a die, using `roll` from Chapter 1. 
7. Use the `replicate` function to produce an array.
8. Use the `roll` function 1000 times to check the fairness of your dice.
9. Use the `prob` argument of the `sample` function to weight your dice.
10. Use `qplot` to plot the histogram of results of your weighted dice.

### Chapter 3
