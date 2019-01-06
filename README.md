# DataBricks_Certiification

Cheat Sheet of the exam


** General Understanding **

7-steps-for-a-developer-to-learn-apache-spark.pdf and videos(associated)


**Terms to Understand**

Catalyst Optimizer
https://databricks.com/glossary/catalyst-optimizer

Tungsten
https://databricks.com/glossary/tungsten


Wide-vs-Narrow-Dependencies
https://github.com/rohgar/scala-spark-4/wiki/Wide-vs-Narrow-Dependencies


Data Serialization
Serialization plays an important role in the performance of any distributed application. Formats that are slow to serialize objects into, or consume a large number of bytes, will greatly slow down the computation. Often, this will be the first thing you should tune to optimize a Spark application. Spark aims to strike a balance between convenience (allowing you to work with any Java type in your operations) and performance. It provides two serialization libraries:

Java serialization: By default, Spark serializes objects using Java’s ObjectOutputStream framework, and can work with any class you create that implements java.io.Serializable. You can also control the performance of your serialization more closely by extending java.io.Externalizable. Java serialization is flexible but often quite slow, and leads to large serialized formats for many classes.
Kryo serialization: Spark can also use the Kryo library (version 4) to serialize objects more quickly. Kryo is significantly faster and more compact than Java serialization (often as much as 10x), but does not support all Serializable types and requires you to register the classes you’ll use in the program in advance for best performance.



**Performance Tunining***
apache-spark-best-practices-and-tuning.pdf(read once)
https://qubole.zendesk.com/hc/en-us/articles/216920846-How-To-Spark-SQL-Tuning
