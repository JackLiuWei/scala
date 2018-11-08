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
		//内部类可以直接访问
		class InnerMost{
			f()
		}
	}
	//外部类不能访问私有属性
	//(new Inner).f()
}
```
### 3 protect访问控制符号
```javascript
package p{
	class Super{
		//protected修饰类方法
		protected def f(){ println("AAAAAAAAAAAA")}
	}
	//子类可以访问
	class Sub extends Super{
		f()
	}
	//普通类无法直接在内部访问
	class Other{
		//(new Super).f()   //错误
	}
}
```
### 4 作用域保护
```javascript
package bobsrockets{
	package navigation{
		private[bobsrockets] class Navigator{
			protected[navigation] use starChart{}
			class LegOfJourney{
				private[navigator] val distance = 100;
			}
			private[this] var speed = 200;
		}
	}
	package lunch{
		//导入navigation包中的Navigator类
		import navigation._
		Object Vehicle{
			private[lunch] val guide = new Navigator
		}
	}
}
```

### 方法与函数
```javascript
object add{
	//传入必要的参数，并定义返回值类型
	def addF(x:Int,y:Int):Int = {
		var sum:Int=0
		sum = x+y
		return sum
	}
	def main(args:Array[String]){
		//调用函数
		println(addF(1000,240))
	}
}
```
