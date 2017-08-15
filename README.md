# spark
spark
spark val topWordCount = hamlet.flatMap(str=>str.split(“ “)). filter(!_.isEmpty).map(word=>(word,1)).reduceByKey(_+_).map{case (word, count) => (count, word)}.sortByKey(false)
