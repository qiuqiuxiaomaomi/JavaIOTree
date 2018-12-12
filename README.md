# JavaIOTree
Java的输入输出流技术研究


![](https://i.imgur.com/K4QhT8w.png)

<pre>
流：
          流是一组由顺序的，有起点和终点的字节集合，是对数据传输的总称或抽象，即数据在两
      设备间的传输称为流，流的本质是数据传输，根据数据传输特性将流抽象为各种类，方便更直观
      的进行数据操作。
</pre>

<pre>
IO流的分类：
      根据处理数据类型的不同分为：
                              1）字符流
                              2）字节流

      根据数据流向的不同分为：
                          1）输入流
                          2）输出流
</pre>

<pre>
字符流 VS 字节流

      字符流的由来：因为数据编码的不同，而有了对字符进行高效操作的流对象，本质其实就是基于
                  字节流读取时，去查了指定的码表，字节流和字符流的区别：
      
      1）读写单位不同：字节流以字节为单位，字符流以字符为单位，根据码表映射自己，一次可能读
                     取多个字节。
      2）处理对象不同：字节流能处理所有类型的数据，如图片，avi等，而字符流只能处理字符类型
                     的数据。

      结论：只要是纯文本数据，就优先考虑字符流，除此之外使用字节流。
</pre>

<pre>
字节流：
      输入：
          InputStream;
          ByteArrayInputStream,StringBufferInputStream,FileInputStream,PipedInputStream  
          ObjectInputStream;
      输出：
          OutputStream;
          ByteArrayOutputStream, FileOutputStream,PipedOutputStream
          ObjectOutputStream,FilterOutputStream
<pre>
字符流：
      输入：
          Reader;
          CharReader, StringReader,PipedReader;
          BufferedReader;
          FilterReader;
          InputStreamReader

      输出：
          Writer;
          CharArrayWriter;
          BufferedWriter;
          PrintWriter,PrintWriteStream;
          OutputStreamWriter;
</pre>

<pre>
字符流与字节流的转换

     转换流的特点：
                1）其是字符流和字节流之间的桥梁
                2）可对读取到的字节数据经过指定编码转换成字符。
                3）可对读取到的字符数据经过指定编码转换成字节流。

     InputStreamReader:字节流到字符流的转换；
     OutPutStreamWriter:字符流到字节流的转换；
</pre>