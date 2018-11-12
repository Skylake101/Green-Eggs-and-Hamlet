# SparkPro5

## About Me & Objective
I'm Luke Carlson, I am a Junior from Northwest Missouri. This assignment is helping us learn how to use Spark and Scala. I also like to spend a lot of time with my fridge door open, looking inside of my fridge without actually getting anything.

## My raw data with a link to original source
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
The output I got from entering 5 words was:

the	986
and	685
of	621
to	604
I	513

'The' was used 986 times making it the most frequent.

![chart](URL)
