
## System.getProperty("")
``` 
line.separator   换行符，\r\n windows;\r Mac; \n Linux/Unix 例：System.getProperty("line.separator")


```



## 获取系统换行符
```
/**  
 * 获取当前系统的换行符  
 */    
public static void lineSeparator() {    
//注意在将流写入文件时，换行应根据操作系统的不同来决定。    
//在程序我们应尽量使用System.getProperty("line.separator")来获取当前系统的换    
//行符，而不是写/r/n或/n。    
//这样写程序不够灵活    
//当我们在java控制台输出的时候，/r和/n都能达到换行的效果。    
if (System.getProperty("line.separator").equals("/r/n")) {    
    System.out.println("//r//n is for windows");    
} else if (System.getProperty("line.separator").equals("/r")) {    
    System.out.println("//r is for Mac");    
} else if (System.getProperty("line.separator").equals("/n")) {    
    System.out.println("//n is for Unix/Linux");    
}    
    
System.out.println("aa/nbb");    
System.out.println("aa/rbb");    
System.out.println("aa/tbb");
```