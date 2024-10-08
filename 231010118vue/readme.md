1.创建vue实例

2.文本插值
	<tag>{{表达式}}</tag>
	文本
	html不能渲染
3.内置指令
	<tag v-指令名[:属性][="表达式"]></tag>
	(1)内容
	v-pre
	v-once
	v-text：渲染文本
	v-html：html渲染
	(2)动态属性
	v-bind	缩写（语法糖）:
	<img v-bind:src="URL"/> === <img :src="URL"/>
	v-bind:style="{}"
	v-bind:class	可以与class叠加
	用法：0/1 v-bind:class="{类名:逻辑表达式,类名2:逻辑表达式2,……}"
		  1/2 v-bind:class="逻辑表达式?'true时类名':'false时类名'"
		  多选 v-bind:class="[类表达式1,类表达式2,……]"
	(3)事件  
	v-on:事件类型="简单语句"
	v-on:事件类型="自定义函数"
	定义函数：
	data(){
		return{
			
		}
	},
	methods:{
		function(){},
	}
	(4)列表渲染
	v-for="循环变量 in/of 总的数据项"
	v-for="(数组元素,数组下标) in/of 数组"