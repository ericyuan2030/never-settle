# loganc++项目学习


## 1.各文件分析

### 1. json_util.c 和 json_util.h

	#ifndef CLOGAN_JSON_UTIL_H
	#define CLOGAN_JSON_UTIL_H
	#endif 


![2023-11-15_1d96b7f1e84e.jpg](https://cdn.jsdelivr.net/gh/EricYuan1201/img@main/2023-11-15_1d96b7f1e84e.jpg)

## 2. 分析

	1. 定义了一种结构体 cLogan_model
	2. 先初始化
	3. 写到mmap内存区域
	4. 写到文件中
	5. 


## 5. 基础语法


	1. malloc： memory allocate 进行分配内存，如果内存不足，会返回null.
	2. memset(item, 0, sizeof(Json_map_logan))，从item开始，设置0，大小为sizeof()
	3. memcmp(item, &temp, sizeof(Json_map_logan), 从item开始，比较&temp，大小为sizeof
	4. temp->type，指针调用结构体的属性，进行赋值以及取值。
	5. free(item) 释放内存



