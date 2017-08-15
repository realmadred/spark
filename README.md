# spark
spark
spark val topWordCount = hamlet.flatMap(str=>str.split(“ “)). filter(!_.isEmpty).map(word=>(word,1)).reduceByKey(_+_).map{case (word, count) => (count, word)}.sortByKey(false)

#2
注意编译的scala版本要和spark上的jar版本一样
java.lang.ClassNotFoundException: scala.runtime.java8.JFunction2$mcIII$sp
// 版本需要和spark启动的时候显示的一样
scalaVersion := "2.11.8"
libraryDependencies += "org.apache.spark" %% "spark-core" % "2.2.0"

spark-submit --class "com.spark.SparkPi" spark_2.11-0.1.jar
