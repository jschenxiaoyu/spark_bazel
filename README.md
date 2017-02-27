# spark_bazel
spark example project using bazel build.

# usage
```
git clone --recurse-submodules https://github.com/jschenxiaoyu/spark_bazel.git
```

First, build the spark-all.jar file.
```
cd spark_all_jar
sbt assembly

cp target/scala-2.11/spark-assembly-1.0.jar ../spark_bazel/lib/spark-all-2.10.jar
cd ..
```

Build spark application jar:
```
cd spark_bazel
bazel build //:main

cd ..
spark-submit --class SimpleApp --master local spark_bazel/bazel-bin/main.jar
```
