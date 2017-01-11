---
layout: post
title: "Hello Github Pages"
categories: talk
tags: talk
excerpt: 第一篇文章。
---

Hello ! 随便写写，主要想记录一下`python`, `javascript`, `java` 等等it技术相关的文章。偶尔会发一些其他类的文章。

#### 下面随便贴点代码

``` python
#!/usr/bin/env python
# -*- coding: utf-8 -*-
import os
import time

def check():
    p = 0
    while True:
        f = open("log.txt", "r+")
        f1 = open("result.txt", "a+")
        f.seek(p, 0)
        
        #readlines()方法
        filelist = f.readlines()
        if filelist:
            for line in filelist:
                #对行内容进行操作
                f1.write(line)

        #获取当前位置，为下次while循环做偏移
        p = f.tell()
        print 'now p ', p
        f.close()
        f1.close()
        time.sleep(2)

if __name__ == '__main__':
    check()


```

#### 再来一段

``` java
    
import java.util.ArrayList;  
import java.util.Arrays;  
import java.util.Collections;  
import java.util.Comparator;  
import java.util.HashMap;  
import java.util.List;  
import java.util.Map;  
import java.util.Map.Entry;  
  
 public class SortSomeThing{
     public static void main(String[] args){ 
         Map<String, Long> map = new HashMap<String, Long>();  
         map.put("c", 33333L);  
         map.put("a", 11111L);  
         map.put("d", 44444L);  
         map.put("e", 55555L);  
         map.put("b", 22222L);  
           
         //将map.entrySet()转换成list  
         List<Map.Entry<String, Long>> list = new ArrayList<Map.Entry<String, Long>>(map.entrySet());  
         Collections.sort(list, new Comparator<Map.Entry<String, Long>>() {  
             //降序排序  
             @Override  
             public int compare(Entry<String, Long> o1, Entry<String, Long> o2) {  
                 //return o1.getValue().compareTo(o2.getValue());  
                 return o2.getValue().compareTo(o1.getValue());  
             }  
         });  
   
         for (Map.Entry<String, Long> mapping : list) {  
             System.out.println(mapping.getKey() + ":" + mapping.getValue());  
         }
     }
 } 


```
