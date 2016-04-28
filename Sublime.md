#Sublime中编译运行Java
#1. 在jdk/bin目录下新建runJava.bat
@ECHO OFF  
cd %~dp1  
ECHO Compiling %~nx1.......  
IF EXIST %~n1.class (  
  DEL %~n1.class  
)  
javac %~nx1
IF EXIST %~n1.class (  
  ECHO -----------OUTPUT-----------  
  java %~n1  
) 

#2. 编辑javaC.sublime-build  
{  
	"cmd": ["runJava.bat","$file"],  
	"file_regex": "^(...*?):([0-9]*):?([0-9]*)",  
	"selector": "source.java",  
	"encoding": "936"  
}

#3. 其他问题  
##编译成功但不运行  
要注意sublime中java文件的保存名应该与public类名相同前。使用java命令进行编译，会生成一个class文件，与源文件中的public类同名，只有在Public类与源文件同名时，才能找到正确的class文件并执行。
##保存
如果不保存，直接编译，会将文件保存到Sublime Text\Packages\Java中的Ant.sublime-build文件，出现错误如下：  
javac: 无效的标记: Ant.sublime-build  
用法: javac <options> <source files>  
-help 用于列出可能的选项
