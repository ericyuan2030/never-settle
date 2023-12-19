# 同步异步IO

## 核心概念理解

1. Tomcat 默认是同步 IO。
    
    ![https://cdn.jsdelivr.net/gh/EricYuan1201/img@main/2023-03-29_d8c01f1dc397.jpg](https://cdn.jsdelivr.net/gh/EricYuan1201/img@main/2023-03-29_d8c01f1dc397.jpg)
    
    ![https://cdn.jsdelivr.net/gh/EricYuan1201/img@main/2023-03-29_d4fd642838b7.jpg](https://cdn.jsdelivr.net/gh/EricYuan1201/img@main/2023-03-29_d4fd642838b7.jpg)
    
2. 改造后台，改造成 Reactor 的方式，实现非阻塞性 IO。核心是 Flux + Mono。
    
    ![https://cdn.jsdelivr.net/gh/EricYuan1201/img@main/2023-03-29_c18617f4b074.jpg](https://cdn.jsdelivr.net/gh/EricYuan1201/img@main/2023-03-29_c18617f4b074.jpg)
    

## 结论

1. Tomcat 默认是同步 IO。
2. 可以改造后台，改成 Reactor 的方式，实现非阻塞性 IO。
3. 核心是 Flux + Mono。