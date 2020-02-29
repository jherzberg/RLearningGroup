## Welcome!

Read this page to join our group! Each week we read one textbook chapter and then discuss it on Tuesday. You can catch up quickly by reading this page and following the exercises. If you want to study the material more closely, please read any chapters you missed. Feel free to contact me, JLHerzberg, on slack with questions.

We are using this [textbook](https://rstudio-education.github.io/hopr/index.html).

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
<details>
  <summary>Install <code>ggplot</code>, which includes <code>qplot</code>.</summary>
  
    <code>install.packages("ggplot2")</code>
</details>
<details>
  <summary>Import <code>qplot</code>.</summary>
  
    <code>library("ggplot2")</code>
</details>
<details>
  <summary>Plot a scatter plot.</summary>
  
    <code>
    x <- c(-1, -0.8, -0.6, -0.4, -0.2, 0, 0.2, 0.4, 0.6, 0.8, 1)
    y <- x^3
    qplot(x, y)
    </code>
</details>
<details>
  <summary>Plot a histogram.</summary>
  
    <code>
    qplot(x, binwidth=1)
    </code>
</details>
<details>
  <summary>Explain how the <code>binwidth</code> argument works.</summary>
  
    The first bin is defined by a left open bound on the least element of the list, and a right closed bound <code>binwidth</code> greater than the least element. Then each successive bin has range <code>binwidth</code> and two closed bounds.
</details>
<details>
  <summary>Use the <code>replicate</code> function to produce 10 rolls of a die, using `roll` from Chapter 1. </summary>
  
    <code>
    replicate(10, roll())
    </code>
</details>
<details>
  <summary>Use the <code>replicate</code> function to produce an array.</summary>
  
    <code>
    replicate(3, c(1, 2, 3))
    </code>
</details>
<details>
  <summary>Use the <code>roll</code> function 1000 times to check the fairness of your dice.</summary>
  
    <code>
    rolls <- replicate(10000, roll())
    qplot(rolls, binwidth = 1)
    </code>
</details>
<details>
  <summary>Use the <code>prob</code> argument of the <code>sample</code> function to weight your dice.</summary>
  
    <code>
    roll <- function() {
    die <- 1:6
    dice <- sample(die, size = 2, replace = TRUE, 
      prob = c(1/8, 1/8, 1/8, 1/8, 1/8, 3/8))
    sum(dice)
     }
    rolls <- replicate(10000, roll())
    qplot(rolls, binwidth = 1)
    </code>
</details>

### Chapter 3
<details>
  <summary>Check whether an object is a vector, atomic, and then find its length.</summary>
  
    <code>
    v = c(1, 2, 3, 4)
    is.vector(v)
    is.atomic(v)
    length(v)
    </code>
</details>
<details>
  <summary>Make an atomic vector of ints, characters, logicals, and doubles.</summary>
  
    <code>
    x = c(1L, 2L, 3L, 4L)
    x = c("1", "2", "3", "4")
    x = c(TRUE, FALSE, FALSE, TRUE)
    x = c(1, 2, 3, 4)
    </code>
</details>
<details>
  <summary>Make an atomic vector of ints, text, and doubles.</summary>
  
    <code>
    x = c(1L, 2L, 3L, 4L)
    x = c("1", "2", "3", "4")
    x = c(1, 2, 3, 4)
    </code>
</details>
<details>
  <summary>Make an atomic vector of complex and raws.</summary>
  
    <code>
    x = c(i, i, i, i)
    x = raw(4)
    </code>
</details>
<details>
  <summary>Give die <code>names</code> attribute. Then remove them</summary>
  
    <code>
    die <- 1:6
	names(die) <- c("one", "two", "three", "four", "five", "six")
	die
    </code>
    <code>
    names(die) <- NULL
    </code>
</details>
<details>
  <summary>Change die to a <code>2</code> (rows) by <code>3</code> (columns) matrix with <code>dim</code>.</summary>
  
    <code>
    dim(die) <- c(2, 3)
    </code>
</details>
<details>
  <summary>Create a <code>matrix</code> from die with <code>2</code> rows and <code>3</code> (columns).</summary>
  
    <code>
    m <- matrix(die, nrow = 2)
    </code>
</details>
<details>
  <summary>Create an <code>array</code> from die with <code>2</code> rows and <code>3</code> columns.</summary>
  
    <code>
    ar <- array(die, dim = c(2, 3))
    </code>
</details>
<details>
  <summary>Save the current time as an object.</summary>
  
    <code>
    ti <- Sys.time()
    </code>
</details>
<details>
  <summary>Factors store categorical information. Make a factor with two categories of length four.</summary>
  
    <code>
    an <- factor(c("elephant", "tiger", "elephant", "elephant"))
    </code>
</details>
<details>
  <summary>Check the type of a vector defined as <code>c("ace", "spades", 1)</code></summary>
  
    <code>
    c("ace", "spades", 1)
    [1] "ace" "spades" "1"
    </code>
</details>
<details>
  <summary>What is the sum of <code>c(TRUE, TRUE, FALSE)</code>?</summary>
  
    <code>
    [1] 2
    </code>
</details>
<details>
  <summary>Lists won't coerce types. Make a card with <code>list</code>.</summary>
  
    <code>
    card <- list("ten", "clubs", 10)
    </code>
</details>
<details>
  <summary>Data frames store data well. Store some cards in a data frame.</summary>
  
    <code>
    df <- data.frame(face = c("ace", "two", "six"),  
  					 suit = c("clubs", "clubs", "clubs"), 
  					 value = c(1, 2, 3)
  					)
    </code>
</details>
<details>
  <summary>Import a csv into R.</summary>
  
    Click "Import Dataset" in the top right. Then click "From Text File". Then click "Import" in the bottom right.
</details>
<details>
  <summary>Save your data frame as a csv.</summary>
  
    <code>
    write.csv(df, file = "threecards.csv", row.names = FALSE)
    </code>
</details>

