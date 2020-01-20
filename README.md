问题：v-if 和 v-for 哪个优先级高？如果两个同时出现，应该怎么优化得到更好的性能

回答：当和 v-if 一起使用时，v-for 的优先级比 v-if 更高。 但是注意我们不推荐在同一元素上使用 v-if 和 v-for。由于v-for 的级别比 v-if 的级别更高，这就意味着 v-if 将重复运行于 v-for 循环中

优化：

情况一 ：v-if 在 v-for 之后
用计算属性（computed）过滤一遍数据，再用 v-for 循环

情况二 ：v-if 在 v-for 之前
把 v-if 提取放到 v-for 父级标签上。
