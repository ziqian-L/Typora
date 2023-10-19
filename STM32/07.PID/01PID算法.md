参考资料：

[PID控制器 - 维基百科](https://zh.wikipedia.org/zh-cn/PID控制器)



# PID

PID控制器，全称比例-积分-微分控制器。整个控制系统由比例单元，积分单元，微分单元三个单元组成。可以通过调节这三个单元的增益系数$K_p$、$K_i$、$K_d$来调节整个控制器。PID控制器适用于基本上线性，并且动态特性不随时间变化的系统。

PID控制器使用十分灵活。有的应用只需要使用到PID控制器的部分单元，在使用时只需要将不需要控制的单元增益系数设置为0即可。常见的有，PI控制器、PD控制器、P控制器、I控制器。

# 串级、并级PID

## 并级PID，也即是理论上的PID控制器

$$
{\mathrm  {u}}(t)={\mathrm  {MV}}(t)=K_{p}{e(t)}+K_{{i}}\int _{{0}}^{{t}}{e(\tau )}\,{d\tau }+K_{{d}}{\frac  {d}{dt}}e(t)
$$

## 串级PID

串级PID即是串联起来的PID控制器，

# 位置式PID、增量式PID

## 位置式PID

```c
typedef struct 
{
    float Kp;
    float Ki;
    float Kd;
    float SetPoint;  // 设定点
    float LsatError; // 最后的偏差
    float PrevError; // 上一次的偏差
    float SumError;  // 误差的积分
} Incremental_PID_TypeDef;

Incremental_PID_TypeDef PID;

int16_t PID_Contorl(int16_t current_value)
{
    float Error,    //偏差
        dError;     //偏差的微分
    Error = current_value - PID.SetPoint;      //偏差 = 当前值 - 设定值
    PID.SumError += Error;                     //偏差的积分
    dError = Error - PID.LsatError;            //偏差的微分
    PID.LsatError = Error;                     //储存偏差值
    return (PID.Kp * Error +                        //计算PID
            PID.Ki * PID.SumError +
            PID.Kd * dError);
}
```



## 增量式PID

```c

```

