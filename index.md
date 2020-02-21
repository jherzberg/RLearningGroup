## Welcome!

Read this page to join our group! Each week we read one textbook chapter and then discuss it on Tuesday. You can catch up quickly by reading this page and following the exercises. If you want to study the material more closely, please read any chapters you missed. Feel free to contact me, JLHerzberg, on slack with questions.

We are using this [textbook](https://d1b10bmlvqabco.cloudfront.net/attach/ighbo26t3ua52t/igp9099yy4v10/igz7vp4w5su9/OReilly_HandsOn_Programming_with_R_2014.pdf).

Other links: [FAQ](https://jlherzberg.github.io/RLearningGroup/faq.html)

### Chapter 0
You don't need to download R to participate in the weekly discussion. You do need to download R and RStudio to code on your own. Please watch this [video](https://www.youtube.com/watch?v=cX532N_XLIs) to download R and RStudio.

### Chapter 1
<details>
  <summary>Add <code>6</code> and <code>10</code> together with R.</summary>
  
    <code>6+10</code>
</details>
<details>
  <summary>Set the object <code>x</code> equal to <code>8</code>.</summary>
  
    <code>x <- 8 </code> or <code>x = 8</code>
</details>
<details>
  <summary>Set the object die equal to the range of numbers <code>1</code> through <code>6</code>.</summary>
  
    <code>die <- 1:6</code>
</details>
<details>
  <summary>Compare die to the range numbers <code>5</code> through <code>6</code>. </summary>
  
    <code>die == 5:6</code>
</details>
<details>
  <summary>Compute the mean of <code>5</code> and <code>8</code>.</summary>
  
    <code>mean(8, 5)</code>
</details>
<details>
  <summary>Write a comment with <code>#</code>.</summary>
  
    <code># i'm a comment!</code>
</details>
<details>
  <summary>Write a function that rolls two dice with the <code>sample</code> function and returns their sum.</summary>
  
    <code>
    roll <- function() {
     die <- 1:6
     dice <- sample(die, size = 2, replace= TRUE)
     sum(dice)
    }
    </code>
</details>
<details>
  <summary>Rewrite that function with an argument parameter for the number of dice to roll. </summary>
  
    <code>
    roll <- function(num_dice=2) {
     die <- 1:6
     dice <- sample(die, size = num_dice, replace= TRUE)
     sum(dice)
    }
    </code>
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
