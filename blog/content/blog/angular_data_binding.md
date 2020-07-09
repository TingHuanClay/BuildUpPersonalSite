---
title: "Let's take a look on Data Binding in Angular"
date: 2020-07-09T21:58:00+08:00
draft: false

# post thumb
image: "images/post/post-13.jpg"

# meta description
description: "How exactly to do Data Binding"

# taxonomies
categories:
  - "Front-End"
tags:
  - "Angular"
  - "Learning"

# post type
type: "post"
---

因為專案的關係 這陣也開始使用Angular作前端的開發工作  

在學習Angular的過程中，除了跟著官網提供的Hero App Tutorial學習之外  

其實也是邊看既有專案以及網路神人們的教學文章邊學習  

最近打算花點時間 把這陣子學到的經驗記錄下來  

過程中首先遇到需要釐清的部分就是 **Data Binding**  

**Data Binding** 可以用下面這張圖作解釋 (待補)  

基本上就是可以透過 Data Binding 在 HTML 與 Typescript 互相設定值  

而 **Data Binding** 總共有四種方式 也各自有其用槍時機 

接下來就逐一介紹要如何使用與其用槍時機吧

##### 1. Interpolation (內嵌綁定)  

- HTML part

```html
<div> {{name}} </div>
```

- Typescript part

```ts
//...
export class AppComponent {
	name: string = "Clay";
}
//...
```

- 用槍時機
  
##### 2. Prpperty Binding (屬性綁定)  

- HTML part


```html
<div [ngClass]="color">Font color</div>
```

- Typescript part

```ts
//...
export class AppComponent {
    color: string = "blue";
}
//...
```

- 用槍時機
  
  
##### 3. Event Binding (事件綁定)  

- HTML part

```html
<button (click)="onSubmit()">  </button>
```

- Typescript part

```ts
//...
export class AppComponent {
	onSubmit(): void {
		// Do whatever you want to implement ... 
	}
}
```

- 用槍時機
  
  
##### 4. Two-Way Data Binding (雙向綁定)  

- HTML part

```html

<input type="text" [(ngModel)]="name" />

```

- Typescript part

```ts
//...
export class AppComponent {
    name: string = "Clay";
}
//...
```

- 用槍時機
  

以上就是簡單的 Data Binding in Angular 的紀錄跟說明啦  
希望大家也都搞懂了  

---


Ref:

[**Angular 4 教學 - Data Binding**](https://blog.johnwu.cc/article/angular-4-%E6%95%99%E5%AD%B8-data-binding.html)

[**[Angular] Data Binding 是在綁什麼?!**](https://medium.com/@hsien.w.wei/angular-data-binding-%E6%98%AF%E5%9C%A8%E7%B6%81%E4%BB%80%E9%BA%BC-cb73a528c674)


