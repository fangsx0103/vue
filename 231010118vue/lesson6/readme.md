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
		①语法
		v-on:事件类型="简单语句"
		v-on:事件类型="自定义函数"
		②事件类型
		键盘：keydown,keypress,keyup,……
		鼠标：click,dblclick,mouseEnter,mousemove,mouseover,……
		表单：submit,blur,focus,……
		other：……
	
		定义函数：
		data(){
			return{
				
			}
		},
		methods:{
			function(){},
		}
		③参数
			
			特殊参数：事件对象event
				事件对象在实参中不写时，调用函数不能加()
				若参数只有事件对象，可以省略
				若参数	$event + parms=>1,$event 不能省略
				
		④修饰符
		.修饰符
		v-on:事件类型.修饰符1.修饰符2="简单语句"
		.prevent 阻止默认动作
		.stop	阻止冒泡
		.self	自身触发，内层元素不触发
		.capture	
		.once
		.passive
		按键修饰符
		.enter	按下回车键触发
		.tab
		.delete (捕获“Delete”和“Backspace”两个按键)
		.esc
		.space
		.up
		.down
		.left
		.right
	(4)列表渲染
	v-for="循环变量 in/of 总的数据项"
	v-for="(数组元素,数组下标) in/of 数组"