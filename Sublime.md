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
Q：编译成功但不运行？  
A：要注意sublime中java文件的保存名应该与public类名相同，且要把public类放在其他类之前。  
    使用java命令进行编译，会生成一个class文件，与源文件中的第一个类同名。
