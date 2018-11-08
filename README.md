# scala
#### 1 变量
```javascript
object Test {
	val foo = """AAAAAA
	www.runoob.com
	www.w3cschool.cc
	www.runnoob.com
	BBBBBBB"""
	val floatValue = 1e5f 
	val value1 = 3.14159f 
	val value2 = 0xFFFFFFFF
	val value3 = 0777L
	var variableValue : String = "You are kind man!"
	var constantValue : String = "I am Ok !"
	val pa = (10,"Foo")
   def main(args: Array[String]) {
	   println(foo);
	   println(floatValue);
	   println(value1);
	   println(value2);
	   println(value3);
	   println("********************");
	   println(variableValue);
	   println(constantValue);
	   println(pa);
   }
}
```
### 2 private访问控制符
```javascript
class Outer{
	class Inner{
		private def f(){
			println("AAAAAAA")
		}
		class InnerMost{
			f()
		}
	}
	//(new Inner).f()
}
```
