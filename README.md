# spark_bazel
spark example project using bazel build.

# usage
```
bazel build //:main

spark-submit --class SimpleApp --master local bazel-bin/main.jar
```
