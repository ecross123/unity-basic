角度和弧度的关系
-
1 rad(弧度) = 180 / PI ≈ 57.3°

1°(角度) = PI / 180 ≈ 0.01745 rad

所以： 

弧度*57.3 = 角度

角度*0.01745 = 弧度

Unity提供的转化方法
-
```csharp
float rad = 1;
float angle = rad * Mathf.Rad2Deg;
rad = angle * Mathf.Deg2Rad;
```
Unity中三角函数计算只能填弧度
-
```csharp
print(Mathf.Sin(30 * Mathf.Deg2Rad));//0.5
print(Mathf.Cos(30 * Mathf.Deg2Rad));//0.8660254(就是2分之根号3)
//反三角函数则是通过三角函数的结果得到对应的弧度
print(Mathf.Asin(0.5));//30 * Mathf.Deg2Rad
print(Mathf.Acos(0.5));//30 * Mathf.Deg2Rad
```
