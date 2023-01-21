# IntelliJ IDEA实时代码模板(Live Templates)

```java
（1） psvm : 可生成 main 方法
 （2）sout : System.out.println() 快捷输出
 类似的：
 soutp=System.out.println("方法形参名 = " + 形参名);
 soutv=System.out.println("变量名 = " + 变量);
 soutm=System.out.println("当前类名.当前方法");
 “abc”.sout => System.out.println("abc");
 （3）fori : 可生成 for 循环
 类似的：
 iter：可生成增强 for 循环
 itar：可生成普通 for 循环
 （4）list.for : 可生成集合 list 的 for 循环
 List<String> list = new ArrayList<String>();
 输入: list.for 即可输出
 for(String s:list){
 }
 又如：list.fori 或 list.forr
 （5） ifn：可生成 if(xxx = null)
 类似的：
 inn：可生成 if(xxx != null) 或 xxx.nn 或 xxx.null
 （6）prsf：可生成 private static final 
 类似的：
 psf：可生成 public static final
 psfi：可生成 public static final int
 psfs：可生成 public static final String
```

