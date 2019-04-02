## 包

每个 Go 程序都是由包构成的。

程序从 `main` 包开始运行。

本程序通过导入路径 `"fmt"` 和 `"math/rand"` 来使用这两个包。

按照约定，包名与导入路径的最后一个元素一致。例如，`"math/rand"` 包中的源码均以 `package rand` 语句开始。

*注意：* 此程序的运行环境是固定的，因此 `rand.Intn` 总是会返回相同的数字。 （要得到不同的数字，需为生成器提供不同的种子数，参见 [`rand.Seed`](https://go-zh.org/pkg/math/rand/#Seed)。 练习场中的时间为常量，因此你需要用其它的值作为种子数。）

~~~go
package main

import (
	"fmt"
	"math/rand"
)

func main() {
	fmt.Println("My favorite number is", rand.Intn(10))
	//fmt.Println("kjdkjsfk",rand.Intn(10))
}

~~~

## 导入

此代码用圆括号组合了导入，这是“分组”形式的导入语句。

当然你也可以编写多个导入语句，例如：

```
import "fmt"
import "math"
```

不过使用分组导入语句是更好的形式。

~~~go
package main

import (
	"fmt"
	"math"
)

func main() {
	fmt.Printf("Now you have %g problems.\n", math.Sqrt(7))
}

~~~

##  导出名

在 Go 中，如果一个名字以大写字母开头，那么它就是已导出的。例如，`Pizza` 就是个已导出名，`Pi` 也同样，它导出自 `math` 包。

`pizza` 和 `pi` 并未以大写字母开头，所以它们是未导出的。

在导入一个包时，你只能引用其中已导出的名字。任何“未导出”的名字在该包外均无法访问。

执行代码，观察错误输出。

然后将 `math.pi` 改名为 `math.Pi` 再试着执行一次。

~~~
package main

import (
	"fmt"
	"math"
)

func main() {
	fmt.Println(math.Pi)
}

~~~

##  函数

函数可以没有参数或接受多个参数。

在本例中，`add` 接受两个 `int` 类型的参数。

注意类型在变量名 **之后**。

（参考 [这篇关于 Go 语法声明的文章](http://blog.go-zh.org/gos-declaration-syntax)了解这种类型声明形式出现的原因。

~~~
package main

import "fmt"

func add(x int, y int) int {
	return x + y
}

func minus(x int, y int) int {
	return x - y
}

func main() {
	fmt.Println(add(42, 13))
	fmt.Println(minus(42, 13))
}

~~~

## 函数（续）

当连续两个或多个函数的已命名形参类型相同时，除最后一个类型以外，其它都可以省略。

在本例中，

```
x int, y int
```

被缩写为

```
x, y int
```

##  多值返回

函数可以返回任意数量的返回值。

`swap` 函数返回了两个字符串。

##  命名返回值

Go 的返回值可被命名，它们会被视作定义在函数顶部的变量。

返回值的名称应当具有一定的意义，它可以作为文档使用。

没有参数的 `return` 语句返回已命名的返回值。也就是 `直接` 返回。

直接返回语句应当仅用在下面这样的短函数中。在长的函数中它们会影响代码的可读

~~~go
go build：用于编译源码文件，代码包，依赖包；
go run:可以编译并运行go源码文件；
go get:命令主要是用来动态获取远程代码包的；
~~~

