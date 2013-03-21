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
		<div id="menu"></div>
	</header>
	<script src="../build/build.js"></script>
	<script>
		var Menu = require('menu');
		// With positioned menu items we can pull the menu 
		// items from a database and render them in correct order.
		// We may also utilize drag'n'drop features clientside to 
		// rearrange the menu and update the database.   
		var items = {
			'0':{caption:"First",target:"first.html"},
			'1':{caption:"Test",child:{
				'0':{caption:"Something",target:"second.html"},
				'1':{caption:"Third",child:{
					'0':{caption:"Fourth",target:"third.html"}
				}}
			}}
		};	

		var header_menu = new Menu('menu'); 
		header_menu.show(items);
	</script>
</body>
</html>
```