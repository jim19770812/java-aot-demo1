要求jdk11+
jaotc --output libHelloWorld.so HelloWorld.class

会生成一个libHelloWorld.so文件

$ ldd libHelloWorld.so
statically linked

$ java -XX:AOTLibrary=./libHelloWorld.so HelloWorld #以AOT方式执行，注意执行的时候HelloWorld.class文件必须存在
