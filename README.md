# vue-calendar-zy


# Demo

[Demo page](https://jiuyekafei.github.io/vue-calendar/index.html) 



# Installation
# npm

```html
$ npm install vue-calendar-zy
```


# Requirements

- [Vue.js](https://github.com/vuejs/vue) `^2.0.0`
- [moment](https://github.com/moment/moment) `^2.20.1`

```html
import calendar from 'vue-calendar-zy'
Vue.use(calendar);


<template>
	<div id="app">
		<calendar @calendartime="gettime"/>
		or
		<calendar @calendartime="gettime" :userTime="time" userNeedHm="1" :userFormat="format" userLang="zh"/>
	</div>
</template>

<script>
export default {
	name: 'App',
	data (){
		return {
			time : '2018-05-12 20:20',
      format : 'YYYY-MM-DD HH:mm'
		}
	},
	methods : {
		gettime(time){
			this.time = time;
		}
	}
}
</script>
```


# API  
* userNeedHm  
```
userNeedHm   0 or 1 ,default 1 ,is show hour-minute panel
```
* userTime  
```
userTime     '2018-04-11 15:23' or new Date()  , default new Date()   
```
* userLang 
```
userLang     zh or en  ,default zh
```
* userFormat
```
userFormat   time format ,such as 'YYYY-MM-DD HH:mm' or 'YYYY-MM-DD' ,default YYYY-MM-DD HH:mm
```
* calendartime
```
function  get set time
```

# License

[The MIT License](http://opensource.org/licenses/MIT)
