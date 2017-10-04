---
layout: post
title: Angular Components and Data Binding
feature-img: "assets/img/sample_feature_img_2.png"
---

Angular! A JavaScript framework that simplifies front-end development through templating and modularization. 

I started working with Angular towards the end of this summer, hoping to become proficient with the MEAN stack and am picking it up again now that I've adjusted to a very busy course schedule. In doing so, it is important for me to review the basics!

#### What is a componenet?

Well, *everything* is a componenet, but that doesn't quite cover it when just learning Angular.

A componenet is essentially an element that is designed to be reused throught an Angular application. It includes a selector, which is used within the HTML as well as a template. The template determines what exactly will be displayed in the component. This can vary depending on data binding, which I'll get into later.

An example of a component follows

```typescript
import { Component } from '@angular/core';

@Component({
	selector: 'logged-in-user-welcome',
	template:`
		<div>
		{% raw %}Welcome back, {{username}}{% endraw %}
		</div>
		`
	})
```

The first line imports the component decorator from the core module, we need this to define our custom component.

The selector is used within HTML tags to place the componenet wherever necessary. For example,
```html
<logged-in-user-welcome></logged-in-user-welcome>
```