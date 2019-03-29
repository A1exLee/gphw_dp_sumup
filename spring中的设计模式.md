# Spring

## AOP

```java
  //环绕不同文件夹下的mybatis mapper文件设置不同数据源
@Around("execution(* com.alexlee..*.ibm.mybatis.*.*(..))")
    public Object doAroundFirefly(ProceedingJoinPoint jp) throws Throwable {
        MultiDataSource.setDataSourceKey("ibmDatasource");
        return jp.proceed();
    }
   
@Around("execution(* com.alexlee..*.huawei.mybatis.*.*(..))")
    public Object doAroundFirefly(ProceedingJoinPoint jp) throws Throwable {
        MultiDataSource.setDataSourceKey("huaweiDatasource");
        return jp.proceed();
    }
```

## IOC-DI

>  (依赖注入是控制反转的一种实现。由spring进行对象创建后注入，实现了控制反转。)

```java
@Autowired
@Resource
@Service
```