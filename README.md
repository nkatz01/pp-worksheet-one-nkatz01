# Programming Paradigms - Worksheet One
Author @nkatz01  03/10/2019

We will be completing some exercises on the <https://www.scala-exercises.org> site.

1. Got to the site.
2. Login with your nice new shiny `GitHub` account.
3. Follow the [`Scala Tutorial`][tut] path (click on the `Start` button).

For this week you should complete the following exercises:

+ `Terms And Types`
1 + 2 shouldBe 
3


"Hello, " ++ "Scala!" shouldBe 
"Hello, Scala!"


"Hello, Scala!".toUpperCase shouldBe 
"HELLO, SCALA!"

-42.abs shouldBe 
42

1 to 
10


16.toHexString shouldBe 
"10"

(0 to 10).contains(10) shouldBe true
(0 until 10).contains(10) shouldBe 
false

"foo".drop(1) shouldBe "oo"
"bar".take(2) shouldBe 
"ba"

+ `Definitions And Evaluation`

METHODS

def square(x: Double) = x * x

square(3.0) shouldBe 
9

def square(x: Double) = x * x

def area(radius: Double): Double = 3.14159 * square(radius)

area(10) shouldBe 
314.159

def triangleArea(base: Double, height: Double): Double =
  base * height / 
2


triangleArea(3, 4) shouldBe 6.0
triangleArea(5, 6) shouldBe 
15

+ `Functional Loops`

def factorial(n: Int): Int =
  if (n == 
1
) 
1

  else factorial(n - 
1
) * n

factorial(3) shouldBe 6
factorial(4) shouldBe 24

+ `Lexical Scopes`
Exercise: Scope Rules

val x = 0
def f(y: Int) = y + 1
val result = {
  val x = f(3)
  x * x
} + x
result shouldBe 
16

object Foo {
  val x = 1
}
object Bar {
  val x = 2
}
object Baz {
  import Bar.x
  val y = x + Foo.x
}

Baz.y shouldBe 
3

[tut]: https://www.scala-exercises.org/scala_tutorial/terms_and_types
