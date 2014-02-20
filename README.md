*This repository is a mirror of the [component](http://component.io) module [kaerus-component/menu](http://github.com/kaerus-component/menu). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/kaerus-component-menu`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*
Menu
====

Nested menu

<p align="center">
  <img src="https://raw.github.com/kaerus-component/menu/master/screenshot.png"/>
</p>

```html
<!doctype html>
<head>
	<title>Top header menu</title>
	<link rel="stylesheet" href="../build/build.css" />
	<link rel="stylesheet" href="./stylesheet.css" />
</head>
<body>
	<header>
		<nav id="menu"></nav>
	</header>
	<script src="menu.js"></script>
	<script>
		var Menu = new (require('menu'))();

		var items = [
			{caption:"Test",child:[
				{caption:"Something",id:"something",target:"something.html",shortcut:"[META]S"},
				{caption:"Open File",id:"fileopen",shortcut:"[CTRL]O"},
				{caption:"A very long menu option",id:"long",target:"long.html",shortcut:"[META]L"},
				{},
				{caption:"Third",child:[
					{caption:"Fourth",target:"fourth.html",shortcut:"[ALT]F"},
					{caption:"Fifth",target:"fifth.html",shortcut:"[SHIFT]F"}
				]}
			]}
		];	

		Menu.show(items); 
		
	</script>
</body>
</html>
```


License
=======
```
Copyright (c) 2013 Kaerus (kaerus.com), Anders Elo <anders @ kaerus com>.
```
Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at
 
    http://www.apache.org/licenses/LICENSE-2.0
 
Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.