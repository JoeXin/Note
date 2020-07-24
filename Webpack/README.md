###  webpack了解一下

#### weback基础介绍

webpack配置大致了解

* Entry: 入口，webpack执行构建的第一步将从Entry开始，可抽象成输入

* Module: 模块， 在webpack里一切皆模块，将一个模块对应一个文件。webpack 会根据配置的Entry开始递归找出所有依赖的模块

* Chunk: 代码块，在一个Chunk中是由多个模块组合而成，用于代码的合并与分割

* Loader: 模块转换器，用于把模块原内容按照需求转换成新内容

* Plugin: 扩展插件，在webpack构建流程中的特定时机注入扩展逻辑来改变构建结果或变成你想要的要达到的效果

* Output:输出结果，在webpck经过一系列处理并得出最终想要的代码后输出结果
