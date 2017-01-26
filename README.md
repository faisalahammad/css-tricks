# CSS TRICKS AND MAGIG
Here you got all of CSS tricks what I was figuring out on my projects.

### Control Placeholder color
	input::-webkit-input-placeholder, textarea::-webkit-input-placeholder {
	  color: #fff;
	  opacity: 1;
	}

	input:-moz-placeholder, textarea:-moz-placeholder {
	  color: #fff;
	  opacity: 1;
	}

	N.B: Please add your class or id name before selector to work with specific Form.

### Add Custom Social Icons on WordPress Navigation Menu
	.class {
		text-indent: -9999px;
		background-image: url(http://link.com);
		background-repeat: no-repeat !important;
		margin-right: 10px !important;
		width: 50px;
	}

	.class:hover {
		background-color: transparent !important;
	}

	N.B: Add class on NAV Menu

### Add Caret Icon beside Dropdown menu (Parent li)
	.menu li a:after {
		color: #fff !important;
		content: ' ▼' !important;
	}

	.menu li > a:only-child:after {
		content: '' !important;
	}

	N.B: Replace your class inside of .menu 

### Make Responsive iframe (CSS Code)
	.iframe-container {
		position: relative;
		padding-bottom: 56.25%;
		padding-top: 35px;
		height: 0;
		overflow: hidden;
	}
	.iframe-container iframe {
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
	}

### Make Responsive iframe (via Website)

* Use this site to make responsive -> [Responsive iFrame Generator](http://embedresponsively.com)