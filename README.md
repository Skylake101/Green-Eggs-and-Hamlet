# SparkPro5

## About Me & Objective
I'm Luke Carlson and I'm a Junior at Northwest Missouri, this is Spark Project 5. I am learning how to use Spark and Scala. I am using spark to grab certain words from a text from a text document called Green Eggs and Hamlet.

## Documents pulled
I made my green eggs and Hamlet document using Hamlet.:
- [HAMLET](http://shakespeare.mit.edu/hamlet/full.html "Website for Hamlet")

## Commands I used for Scala
```
scala> val inputFile = sc.textFile("C:/527439/Skylake101/SparkPro5/GreenEggsandHamlet")
scala> val topWordCount = inputFile.



  flatMap(str=>str.split(" ")).
  filter(!_.isEmpty).
  map(word=>(word,1)).
  reduceByKey(_+_).
  map{case (word, count) => (count, word)}.
  sortByKey(false)
scala> topWordCount.take(10).foreach(x=>println(x))
```

## Project Output
The and 'it' was used most frequently. The output I got from entering 5 words was:

1.3068, Then
2.9025, Music
3.2356, We
4.9355, should
5.3528, know
