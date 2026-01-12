基础概念
-
Unity的Mathf和C#的Math都是提供工具用来进行数字计算的，区别在命名空间：Math-System||Mathf-UnityEngine

区别在于Math是C#的类，主要提供了数学的计算方法，而Mathf是由Unity封装的结构体，除了数学计算还有一些适用于游戏开发的方法

所以Unity开发中用Mathf就足够了

Mathf的常用方法
-
```cs
Using UnityEngine;
//一般只计算一次的方法
//1.Π PI
print(Mathf.PI);//3.1415926535
//2.取绝对值 Abs
print(Mathf.Abs(-1));//1
//3.向上取整 CeilToInt
print(Mathf.CeilToInt(1.3f));//2
//4.向下取整 FloorToInt
print(Mathf.FloorToInt(1.3f));//1,也可以强转int i = (int)1.3f就是1
//5.钳制函数 Clamp
print(Mathf.Clamp(10,11,20));//11,Mathf.Clamp(当前值,最小值,最大值)，用来限定某个参数的范围不让它超过你设定的边界
//6.获取最大值 Max
print(Mathf.Max(1,2,3,4));//4,多个也可以它有可变长参数的重载params int[] values
//7.获取最小值 Min
print(Mathf.Max(1,2,3,4));//1
//8.n次幂 Pow
print(Mathf.Pow(4,3));//64,参数一是底数，参数二是幂数
//9.四舍五入 RoundToInt
print(Mathf.RoundToInt(1.49f));//1
//10.平方根 Sqrt
print(Mathf.Sqrt(4));//2
//11.判断是否是2的n次方 IsPowerOfTwo
print(Mathf.IsPowerOfTwo(4));//true
print(Mathf.IsPowerOfTwo(3));//false
//12.判断正负 Sign
print(Mathf.Sign(10));//1
print(Mathf.Sign(0));//1
print(Mathf.Sign(-10));//-1
```
Mathf中需要不停运算的方法——插值运算Lerp
-
公式：
result = Mathf.Lerp(start, end, t);

result = start + (end - start)*t;
其中t是插值系数
```cs
float start, result, time;
//用法一每帧改变start的值，速度快后慢无限接近但是不会达到end目标值
start = Mathf.Lerp(start, 10, Time.deltaTime);
//用法二每帧改变t的值，匀速变化，每帧都接近目标值，当t>=1时达到end
time += Time.deltaTime;
result = Mathf.Lerp(start, 10, time);
```
