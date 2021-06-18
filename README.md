# Green Eggs and Hamlet

## Project Goal
This project uses a combination of Spark and Scala to process words from any 'text' entry. For example: Green Eggs and Ham or Hamlet. It's currently setup to use Hamlet

## My raw data with a link to original source
I made my green eggs and Hamlet document using this website:
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

|Frequency| Item |
|---------|------|
| 986     | the  |
| 685     | and  |
| 621     | of   |
| 604     | to   |
| 513     | I    |

'The' was used 986 times making it the most frequent.

![chart](https://github.com/Skylake101/SparkPro5/blob/master/FrequencyTable.jpg)
