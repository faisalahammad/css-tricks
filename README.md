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
	First put your iframe inside of "iframe-container" class then write custom css on your child theme or external css file.
	
	Example:
	<div class="iframe-container">
		<iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d29192.452902694364!2d90.49141269583086!3d23.852123360864066!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3755cbe13e12ca1b%3A0xe440738bb6817d87!2sPurbachal+New+Town!5e0!3m2!1sen!2sbd!4v1485459233926" width="600" height="450" frameborder="0" style="border:0" allowfullscreen></iframe>
	</div>

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