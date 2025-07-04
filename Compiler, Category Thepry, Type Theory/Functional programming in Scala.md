## Goal 

Learn **Functional Programming** and Scala, using the "Red book"
## Deadlines
### **July 2025**
- 📚 **Week 1 (July 1–7)**: 
  - Read 2–3 chapters of *FP in Scala*
  - Implement `List`, `Tree`, and `Map` in Scala
- 🔧 **Week 2 (July 8–14)**:
  - Job starts (40h/week)
  - Build arithmetic expression evaluator
- 🧠 **Weeks 3–4 (July 15–21)**:
  - State monad simulation project
  - Design grammar for mini language *(a subset of Gleam)*
## 02.07.2025

**Progress:** 9%
**Exercises**:
- [x] fibonacci recursive
**What's new**: remembered recursion, and shamefully forgot how to write fibonacci function

## 03.07.2025

**Progress**: 11%, Chapter 2 finished
**Exercises**:
- [x] curry, uncurry, compose
- [x] isSorted polymorphic function
**What's new**: i think i understand how currying works (?) and that in implementation of it we actually just return a lambda, no black magic here, so i also kinda understand how to take functions as arguments and return them

## 04.07.2025
**Progress**:
**Exercise**:
- [x] tail
- [x] setHead
- [x] drop
- [x] dropWhile
- [x] init 
**What's new**:
This function broke me:
```Scala
  def concat(that : MList[A]) : MList[A] = list match {
    case MList.MNil => that
    case MList.Cons(h, t) => MList.Cons(h, t.concat(that))
  }
```
I have to remember: we can use recursion not only as the last call, but apply it to a part of argument (part of a list) and then it would collapse and when pattern is exhausted start wrapping up the result bottom-up
take this function:
```Scala
// mplement a function, `init`, that returns a `List` consisting of all but the last element of a `List`, so given `List(1,2,3,4)`, `init` will return `List(1,2,3)`.
def init[A](as : MList[A]) : MList[A] = {
  as match {
    case Cons(_, MNil) => MNil
    case Cons(x, xs) => Cons(x, init(xs))
  }
}
```

And vizualize it as this
![[Pasted image 20250704151431.png]]

Also, `foldRight` is `right` because it start callapsing from right to left, see:
```Scala
def foldRight[A, B](as: List[A], acc: B, f: (A, B) => B): B =
  as match
    case Nil => acc
    case Cons(x, xs) => f(x, foldRight(xs, acc, f))

foldRight(Cons(1, Cons(2, Cons(3, Nil))), 0, (x,y) => x + y)
1 + foldRight(Cons(2, Cons(3, Nil)), 0, (x,y) => x + y)      ①
1 + (2 + foldRight(Cons(3, Nil), 0, (x,y) => x + y))
1 + (2 + (3 + (foldRight(Nil, 0, (x,y) => x + y))))
1 + (2 + (3 + (0)))
6
```
> Remember that braces around expressions `1 - ( 2 - (3 - 0 ) )` matter! 

