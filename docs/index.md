---
layout: post
---

<html lang="en">
	<head>
		<meta charset="utf-8">
		<meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
		<meta http-equiv="x-ua-compatible" content="ie=edge">
		<meta name="msvalidate.01" content="89359D9C492A475C0061398008D105FB" />
		
		<!-- seo !-->
		<meta name="description" content="Learn how to use Entity Framework Bulk Insert with Tutorials & Examples for Code First & Database First.">
		<meta name="keywords" content="Entity Framework, Entity Framework Tutorial, Entity Framework Example, Entity Framework Code First, Entity Framework Database First, Entity Framework Bulk Insert, Entity Framework SaveChanges, Entity Framework Performance">
		<title>Entity Framework Bulk Insert, Tutorials, and Examples. Support Entity Framework 6 Code First & Database First.</title>
		
		<!-- icon/css !-->
		<link rel="icon" type="image/png" href="http://entityframework-plus.net/images/logo.png">
		<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0-alpha.6/css/bootstrap.min.css" integrity="sha384-rwoIResjU2yc3z8GV/NPeZWAv56rSmLldC3R/AZzGRnGxQQKnKkoFVhFQhNUwEyJ" crossorigin="anonymous">
		<link rel="stylesheet" type="text/css" href="https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css" />
		<link rel="stylesheet" type="text/css" href="http://entityframework-plus.net/css/github2.css">
		<link rel="stylesheet" type="text/css" href="http://entityframework-plus.net/css/default.1.3.css">
	</head>
	
	<body>
		
<style>
.header * {
	font-family: -apple-system,system-ui,BlinkMacSystemFont,"Segoe UI",Roboto,"Helvetica Neue",Arial,sans-serif;
}
.header .fa-cloud-download {
	font-family: FontAwesome;
}

.header {
	background-color: #fff;
    box-shadow: 0 5px 5px 0 rgba(0, 0, 0, 0.3);
}
.header nav {
	min-height: 100px;
}
.header nav .navbar-brand {
	font-size: 26px;
	font-weight: 300;
}
.header nav .navbar-brand a {
	color: #000;
	text-decoration: none;
}
.header nav .nav-item {
	padding-left: 1em;
	padding-right: 1em;
}
.header nav .nav-item a.nav-link {
	color: #000;
	font-size: 18px;
	font-weight: 300;
	padding-left: 0px;
	padding-right: 0px;
}
.header nav .nav-item-download {
	padding-left: 60px;
	padding-right: 0px;	
}
@media (min-width: 992px) {
	.header a.nav-link {
		position: relative;
		text-decoration: none;
	}
	.header a.nav-link::after {
		border-bottom: 2px solid #c00;
		bottom: 0;
		content: "";
		left: 0;
		position: absolute;
		transition: all 0.5s ease 0s;
		width: 0;
	}
	.header a.nav-link:hover::after {
		width: 100%;
	}
}
@media (max-width: 991px) {
	.header nav .nav-item-download {
		padding-left: 0px;
		margin: auto;
		margin-top: 20px;
		margin-bottom: 10px;
	}
	.header nav {
		min-height: 60px;
	}
}
@media (max-width: 767px) {
	.header nav .navbar-brand {
		font-size: 22px;
	}
}
@media (max-width: 575px) {
	.header nav .navbar-brand {
		font-size: 15px;
	}
}
.text-red {
	color: #c00;
}

.text-green {
	color: #5cb85c;
}
</style>
	
<!-- header !-->
	<div class="header fixed-top">
		<nav class="container navbar navbar-toggleable-md navbar-light">
			<button class="navbar-toggler navbar-toggler-right" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
				<span class="navbar-toggler-icon"></span>
			</button>

			<div class="navbar-brand">
				<a href="http://entityframework-extensions.net">
					<img src="http://entityframework-plus.net/images/logo.png" />
					Entity Framework
					<span class="text-red">Extensions</span>
				</a>
			</div>
			
			<div class="navbar-collapse collapse justify-content-end" id="navbarSupportedContent">			
				<ul class="navbar-nav">
					<li class="nav-item">
						<a class="nav-link" href="http://entityframework-extensions.net/#feature">Features</a>
					</li>
					<li class="nav-item">
						<a class="nav-link" href="http://entityframework-extensions.net/documentation">Tutorials</a>
					</li>
					<li class="nav-item">
						<a class="nav-link" href="http://entityframework-extensions.net/#pricing">Buy</a>
					</li>
					<li class="nav-item">
						<a class="nav-link" href="mailto:info@zzzprojects.com">Contact</a>
					</li>
					<li class="nav-item nav-item-download">
						<a class="btn btn-success btn-lg" href="https://www.nuget.org/packages/Z.EntityFramework.Extensions/" role="button" onclick="ga('send', 'event', { eventAction: 'download'});"><i class="fa fa-cloud-download"></i>&nbsp;NuGet Download</a>
					</li>
				</ul>
			</div>	
		</nav>
	</div>
	
	<div style="height: 100px;">
	</div>
		
		<header>
			<div class="container">
				<div class="row">
					<div class="col-lg-6">
						<div class="card">
							<div class="card-block">
								<hr class="m-y-md" />
								<h2>Dramatically Improve EF Performance with Bulk SaveChanges and Bulk Operations</h2>
								<hr class="m-y-md" />
								<div class="lead">
									<a href="https://www.nuget.org/packages/Z.EntityFramework.Extensions/" target="_blank" class="btn btn-success btn-lg btn-left" role="button" onclick="ga('send', 'event', { eventAction: 'download'});"><span><i class="fa fa-cloud-download fa-2x"></i>&nbsp;<span>Download</span></span></a>
									<br />
									<a href="https://www.nuget.org/packages/Z.EntityFramework.Extensions/" target="_blank" onclick="ga('send', 'event', { eventAction: 'download'});"><img src="https://zzzprojects.github.io/images/nuget/entity-framework-extensions-v.svg" alt="download" /></a>
									<a href="https://www.nuget.org/packages/Z.EntityFramework.Extensions/" target="_blank" onclick="ga('send', 'event', { eventAction: 'download'});"><img src="https://zzzprojects.github.io/images/nuget/entity-framework-extensions-d.svg" alt="" /></a>				
									<div class="text-muted">* PRO Version unlocked for the current month</div>
								</div>
							</div>
						</div>
					</div>
					<div class="col-lg-6">
						<div class="card">
							<br />
							<div class="card-block card-code">
{% highlight csharp %}
// Easy to use
context.BulkSaveChanges();

// Easy to customize
context.BulkSaveChanges(bulk => bulk.BatchSize = 100);

// Perform Bulk Operations
context.BulkDelete(customers);
context.BulkInsert(customers);
context.BulkUpdate(customers);

// Customize Primary Key
context.BulkMerge(customers, operation => {
   operation.ColumnPrimaryKeyExpression = 
        customer => customer.Code;
});
{% endhighlight %}
							</div>
						</div>
					</div>
				</div>
			</div>
		</header>
		
		<!-- featured !-->
		<div id="featured">
			<div class="container">
			
				<!-- Improve Performance !-->
				<h2>Improve SaveChanges Performance</h2>
				<div class="row">
					<div class="col-lg-5">
						<p class="featured-tagline">Use <span class="text-bold-red">scalable</span> bulk operations and always get the best <span class="text-bold-red">performance</span> available for your database provider.</p>
						<ul class="featured-list-sm">
							<li>SQL Server 2008+</li>
							<li>SQL Azure</li>
							<li>SQL Compact</li>
							<li>MySQL</li>
							<li>SQLite</li>
							<li>PostgreSQL</li>
							<li>Oracle</li>
						</ul>	
					</div>
					<div class="col-lg-7">
						<table class="table table-striped table-hover table-responsive">
							<tr class="thead-inverse">
								<th>Operations</th>
								<th>1,000 Entities</th>
								<th>2,000 Entities</th>
								<th>5,000 Entities</th>
							</tr>
							<tr>
								<th>SaveChanges</th>
								<td>1,000 ms</td>
								<td>2,000 ms</td>
								<td>5,000 ms</td>
							</tr>
							<tr>
								<th>BulkSaveChanges</th>
								<td>90 ms</td>
								<td>150 ms</td>
								<td>350 ms</td>
							</tr>
							<tr>
								<th>BulkInsert</th>
								<td>6 ms</td>
								<td>10 ms</td>
								<td>15 ms</td>
							</tr>
							<tr>
								<th>BulkUpdate</th>
								<td>50 ms</td>
								<td>55 ms</td>
								<td>65 ms</td>
							</tr>
							<tr>
								<th>BulkDelete</th>
								<td>45 ms</td>
								<td>50 ms</td>
								<td>60 ms</td>
							</tr>
							<tr>
								<th>BulkMerge</th>
								<td>65 ms</td>
								<td>80 ms</td>
								<td>110 ms</td>
							</tr>
						</table>

						<p class="text-muted">* Benchmark for SQL Server</p>
					</div>
				</div>
			</div>
		</div>
		
		<!-- testimonials !-->
		<div id="testimonials">
			<div class="container">
				<h2>Amazing <span class="text-bold-red">performance</span>, outstanding <span class="text-bold-red">support</span>!</h2>
				<ul>
					<li>- "We were very, very pleased with the customer support. There was no question, problem or wish that was not answered AND solved within days! We think that’s very unique!" Klemens Stelzmüller, <a href="http://www.beka-software.at/" target="_blank">Beka-software</a></li>
					<li>- "I’d definitely recommend it as it is a great product with a great performance and reliability." Eric Rey, <a href="http://www.transturcarrental.com/" target="_blank">Transtur</a></li>
					<li>- "It’s great. It took me 5 minutes to implement it and makes my application 100x more responsive for certain database operations." Dave Weisberg</li>
				</ul>
				<p><a href="http://www.zzzprojects.com/testimonials/" target="_blank" class="btn btn-primary btn-lg" role="button"><span><i class="fa fa-comments"></i>&nbsp;<span>Read More Success Story</span></span></a></p>
				<br /><br />
				<p><span class="text-bold-red">Share</span> your experience. We love to hear from you: <a href="mailto:info@zzzprojects.com">info@zzzprojects.com</a></p>
			</div>
		</div>
		
		<!-- features !-->
		<div id="feature">
			<div class="container">
				
				<!-- BulkSaveChanges !-->
				<a id="bulk-savechanges" href="#"></a>
				<h2>Bulk SaveChanges</h2>
				<div class="row">
					<div class="col-lg-5">
						<p class="feature-tagline">Improving your applications performance couldn’t have been made <span class="text-bold-red">easier</span>!</p>
						<ul>
							<li>Easy to use</li>
							<li>Easy to customize</li>
							<li>Easy to maintain</li>
						</ul>
					</div>
					<div class="col-lg-7">
{% highlight csharp %}
// Easy to use
context.BulkSaveChanges();

// Easy to customize
context.BulkSaveChanges(operation => operation.BatchSize = 1000);
{% endhighlight %}
					</div>
				</div>

				<hr class="m-y-md" />
				
				<!-- Bulk Operations !-->
				<a id="bulk-operations" href="#"></a>
				<h2>Bulk Operations</h2>
				<div class="row">
					<div class="col-lg-5">
						<p class="feature-tagline">Use <span class="text-bold-red">flexible</span> features to overcome Entity Framework limitations</p>
						<ul>
							<li>Choose batch size</li>
							<li>Choose columns</li>
							<li>Choose primary key</li>
						</ul>
						
					</div>
					<div class="col-lg-7">
{% highlight csharp %}
// Use all kind of bulk operations
context.BulkInsert(customers);
context.BulkUpdate(customers);
context.BulkDelete(customers);

// Customize your operation
context.BulkMerge(customers, operation => {
   operation.BatchSize = 1000;
   operation.ColumnPrimaryKeyExpression = customer => customer.Code;
});
{% endhighlight %}	
					</div>
				</div>
				
				<hr class="m-y-md" />
				
				<!-- Flexible Features !-->
				<a id="bulk-from-linq-query" href="#"></a>
				<h2>Bulk from LINQ Query</h2>
				<div class="row">
					<div class="col-lg-5">
						<p class="feature-tagline">Perform bulk operations from LINQ Query without loading entities in the context.</p>
						<ul>
							<li>DeleteFromQuery</li>
							<li>UpdateFromQuery</li>
						</ul>
						
					</div>
					<div class="col-lg-7">
{% highlight csharp %}
// DELETE all customers that are inactive for more than 2 years
context.Customers
    .Where(x => x.LastLogin < DateTime.Now.AddYears(-2))
    .DeleteFromQuery(operation => operation.BatchSize = 10000);
 
// UPDATE all customers that are inactive for more than 2 years
context.Customers
    .Where(x => x.Actif && x.LastLogin < DateTime.Now.AddYears(-2))
    .UpdateFromQuery(x => new Customer {Actif = false});
{% endhighlight %}	
					</div>
				</div>
				
				<!-- more-feature !-->
				<p class="more-feature"><a href="http://www.zzzprojects.com/entity-framework-extensions/docs" target="_blank" class="btn btn-primary btn-lg" role="button"><span><i class="fa fa-book"></i>&nbsp;<span>View More Features</span></span></a></p>
				
			</div>
		</div>
		
		<!-- support !-->
		<a id="supports" href="#"></a>
		<div id="support">
			<div class="container">
				<h2>Test our <span class="text-bold-red">Outstanding</span> Support</h2>
				<h3>We usually answer within the next business day, hour, or minutes!</h3>
				<div class="row">
					<hr class="hidden-sm-up" />
					<div class="col-sm-6 col-lg-3">
						<div class="card">
							<div class="card-block">
								<h4 class="card-title">Contact Us</h4>
							</div>
							<a href="mailto:info@zzzprojects.com"><i class="fa fa-users fa-5x"></i></a>
							<div class="card-block">
								<p class="card-text">Email our team for any questions. We love to hear from you!</p>
								<a href="mailto:info@zzzprojects.com">info@zzzprojects.com</a>
							</div>
						</div>
					</div>
					<hr class="hidden-sm-up" />
					<div class="col-sm-6 col-lg-3">
						<div class="card">
							<div class="card-block">
								<h4 class="card-title">Wiki</h4>
							</div>
							<a href="http://entityframework-extensions.net/documentation" target="_blank" onclick="ga('send', 'event', { eventAction: 'github'});"><i class="fa fa-folder-open fa-5x"></i></a>
							<div class="card-block">
								<p class="card-text">Consult our complete documentation to help you getting started.</p>
								<a href="http://entityframework-extensions.net/documentation" target="_blank" onclick="ga('send', 'event', { eventAction: 'github'});">Wiki</a>
							</div>
						</div>
					</div>
					<hr class="hidden-sm-up" />
					<div class="col-sm-6 col-lg-3">
						<div class="card">
							<div class="card-block">
								<h4 class="card-title">Forum</h4>
							</div>
							<a href="https://github.com/zzzprojects/EntityFramework-Extensions/issues" target="_blank" onclick="ga('send', 'event', { eventAction: 'forum'});"><i class="fa fa-weixin fa-5x"></i></a>
							<div class="card-block">
								<p class="card-text">Visit the forum to report issues, ask questions, and propose new features.</p>
								<a href="https://github.com/zzzprojects/EntityFramework-Extensions/issues" target="_blank" onclick="ga('send', 'event', { eventAction: 'forum'});">Forum</a>
							</div>
						</div>
					</div>
					<hr class="hidden-sm-up" />
					<div class="col-sm-6 col-lg-3">
						<div class="card">
							<div class="card-block">
								<h4 class="card-title">Open Source</h4>
							</div>
							<a href="https://github.com/zzzprojects/EntityFramework-Extensions" target="_blank" onclick="ga('send', 'event', { eventAction: 'github'});"><i class="fa fa-github fa-5x"></i></a>
							<div class="card-block">
								<p class="card-text">Access the partial source of the library you're using. (Under development)</p>
								<a href="https://github.com/zzzprojects/EntityFramework-Extensions" target="_blank" onclick="ga('send', 'event', { eventAction: 'github'});">GitHub</a>
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
		
		<!-- pricing !-->
		<a id="pro" href="#"></a>
		<div id="pricing">
			<div class="container">
				<div class="row">
					<div class="col-lg-6">
						<h2>Pricing</h2>
						<hr class="m-y-md" />
						<p class="pricing-tagline">Join thousands of projects already using bulk operations and make <span class="text-bold-red">YOUR</span> customers happy.</p>
						<ul>
							<li>Improve applications responsivity</li>
							<li>Minimize time your customers wait</li>
							<li>Maximize time your customers work</li>
						</ul>
						<p class="pricing-tagline">"Time Is Money" and your customers expect applications to respond as quickly as possible.</p>											
						<hr class="m-y-md" />
						<p>Every month, a <a href="https://www.nuget.org/packages/Z.EntityFramework.Extensions/" target="_blank" onclick="ga('send', 'event', { eventAction: 'download'});">FREE trial</a> of the PRO version is available to let you evaluate all its features without limitations.</p>
						<hr class="m-y-md" />
						<p>Looking for a <a class="text-bold-red">free & open source</a> library with must-have feature for Entity Framework?</p>
						<p><a href="http://entityframework-plus.net/" target="_blank">Entity Framework Plus</a></p>
						<ul>
							<li>Auditing</li>
							<li>Batch Delete</li>
							<li>Batch Update</li>
							<li>LINQ Dynamic</li>
							<li>Query Cache</li>
							<li>Query Deferred</li>
							<li>Query Filter</li>
							<li>Query Future</li>
							<li>Query IncludeFilter</li>
							<li>Query IncludeOptimized</li>
						</ul>
					</div>
					<div class="col-lg-6">
						<table class="table table-hover table-bordered">
							<thead class="thead-inverse">
								<tr>
									<th>Features</th>
									<th>PRO</th>
								</tr>
							</thead>
							<tbody>
								<tr>
									<th>Bulk SaveChanges</th>
									<td><i class="fa fa-check-square-o fa-2x"></i></td>
								</tr>
								<tr>
									<th>Bulk Insert</th>
									<td><i class="fa fa-check-square-o fa-2x"></i></td>
								</tr>
								<tr>
									<th>Bulk Update</th>
									<td><i class="fa fa-check-square-o fa-2x"></i></td>
								</tr>
								<tr>
									<th>Bulk Delete</th>
									<td><i class="fa fa-check-square-o fa-2x"></i></td>
								</tr>
								<tr>
									<th>Bulk Merge</th>
									<td><i class="fa fa-check-square-o fa-2x"></i></td>
								</tr>
								<tr>
									<th>DeleteFromQuery</th>
									<td><i class="fa fa-check-square-o fa-2x"></i></td>
								</tr>
								<tr>
									<th>UpdateFromQuery</th>
									<td><i class="fa fa-check-square-o fa-2x"></i></td>
								</tr>
								<tr>
									<th>Commercial License</th>
									<td><i class="fa fa-check-square-o fa-2x"></i></td>
								</tr>
								<tr>
									<th>Royalty-Free</th>
									<td><i class="fa fa-check-square-o fa-2x"></i></td>
								</tr>
								<tr>
									<th>Support & Upgrades (1 year)</th>
									<td><i class="fa fa-check-square-o fa-2x"></i></td>
								</tr>
							</tbody>
						</table>
						
						<form action="https://www.paypal.com/cgi-bin/webscr" method="post" target="_top" onsubmit="return purchase_validate()">
							<input type="hidden" name="cmd" value="_s-xclick">
							<input type="hidden" name="currency_code" value="USD">
							<fieldset class="form-group">
								<input type="hidden" name="on0" value="Seats">
								<select id="provider_type" name="hosted_button_id" class="form-control" onchange="selectProduct()">
									<option value="GS977QXB98R2C">SQL Server/ Azure Provider</option>
									<option value="27ML36DSMHEQA">Oracle Provider</option>
									<option value="32JM43GUXW4ZW">MySQL Provider</option>
									<option value="TSCZ2KCM9QBVY">PostgreSQL</option>
									<option value="5WVPWVNDGRHH6">SQL Compact Provider</option>
									<option value="55WDUT7ENJBKU">SQLite Provider</option>
									<option value="TSCGQDC4YR2MQ">ALL Providers</option>
								</select> 
								<br />
								<select id="product_option" name="os0" class="form-control">
									<option id="seat1" value="1 seat">Entity Framework Extensions $599 (1 developer seat)</option>
									<option id="seat2_4" value="2-4 seats" selected>Entity Framework Extensions $799 (2-4 developer seats)</option>
									<option id="seat5_9" value="5-9 seats">Entity Framework Extensions $999 (5-9 developer seats)</option>
									<option id="seat10_14" value="10-14 seats">Entity Framework Extensions $1199 (10-14 developer seats)</option>
									<option id="seat15_19" value="15-19 seats">Entity Framework Extensions $1399 (15-19 developer seats)</option>
								</select> 
							</fieldset>
							<div class="checkbox">
								<label>
									<input id="agree_agreement" type="checkbox">I have read and agree to the <a href="http://www.zzzprojects.com/license-agreement/" target="_blank">License Agreement</a>.
								</label>
							</div>
							<button type="submit" class="btn btn-success btn-lg"><span><i class="fa fa-shopping-cart"></i>&nbsp;<span>BUY NOW</span></span></button>
							<br /><br />
							<p>* Contact us (<a href="mailto:sales@zzzprojects.com">sales@zzzprojects.com</a>) for <span class="text-bold-red">Quote</span>, payment method <span class="text-bold-red">alternative</span>, or major <span class="text-bold-red">bundle discount</span> when purchasing more than one product (or you already bought one).</p>
						</form>					
					</div>
				</div>
			</div>
			
			<!-- validation !-->
			<div id="error_validation" class="modal fade" tabindex="-1" role="dialog" aria-labelledby="modal_agreement" aria-hidden="true">
				<div class="modal-dialog" role="document">
					<div class="modal-content">
						<div class="modal-header">
							<h4 class="modal-title" id="modal_agreement">License Agreement</h4>
						</div>
						<div class="modal-body bg-danger">
							You must read and agree to the License Agreement.
						</div>
						<div class="modal-footer">
							<button type="button" class="btn btn-secondary" data-dismiss="modal">Close</button>
						</div>
					</div>
				</div>
			</div>
		</div>
	
<!-- footer !-->
<footer>
	<div class="container">
		<div class="row">
			<div class="col-lg-6 footer-site-copyright text-center text-lg-left">
				Copyright &copy; 2014 - 2017
				<a href="http://www.zzzprojects.com/">ZZZ Projects Inc.</a> 
				<div class="hidden-lg-up"></div>
				All rights reserved
			</div>
			<hr class="hidden-lg-up">
			<div class="col-lg-6 footer-site-social text-center text-lg-right">
				<a href="https://www.facebook.com/zzzprojects" target="_blank"><i class="fa fa-facebook"></i></a>
				<a href="https://twitter.com/zzzprojects" target="_blank"><i class="fa fa-twitter"></i></a>
				<a href="https://plus.google.com/+Zzzprojects_NetSQL" target="_blank"><i class="fa fa-google-plus"></i></a>
				<a href="http://zzzprojects.us9.list-manage.com/subscribe?u=cecbc4775cf67bf1ff82018af&amp;id=4765ffa5f8" target="_blank"><i class="fa fa-newspaper-o"></i></a>
			</div>
		</div>
	</div>
</footer>
<style>
footer {
	background: rgba(0, 0, 0, 0) linear-gradient(to top, #000, #333) repeat scroll 0 0;
	box-shadow: 0 -8px 8px 0 rgba(0, 0, 0, 0.2);
	color: #777;
	font-weight: 400;
	min-height: 50px;	
	padding: 5px 0;
}
footer a {
    color: #777;
}
footer a:hover {
    color: #777;
    opacity: 0.7;
    text-decoration: none;
    transition: all 0.4s ease-in-out 0s;
}
footer hr {
    margin: 5px;
}
footer .footer-site-copyright {
    padding-top: 4px;
    font-family: -apple-system,system-ui,BlinkMacSystemFont,"Segoe UI",Roboto,"Helvetica Neue",Arial,sans-serif;
}
footer .footer-site-social a {
    font-size: 24px;
    padding: 0 10px;
}
@media (max-width: 61em) {
	footer {
		padding: 20px 0;
	}
}
</style>

<script src="https://code.jquery.com/jquery-3.1.1.min.js" integrity="sha256-hVVnYaiADRTO2PzUGmuLJr8BLUSjGIZsDYGmIJLv2b8=" crossorigin="anonymous"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/tether/1.4.0/js/tether.min.js" integrity="sha384-DztdAPBWPRXSA/3eYEEUWrWCy7G5KFbe8fFjk5JAIxUYHKkDx6Qin1DkWx51bBrb" crossorigin="anonymous"></script>
    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0-alpha.6/js/bootstrap.min.js" integrity="sha384-vBWWzlZJ8ea9aCX4pEW3rVHjgjt7zpkNpZk+02D9phzyeVkE+jo0ieGizqPLForn" crossorigin="anonymous"></script>
 
	<script type="text/javascript">
	  (function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){
	  (i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o),
	  m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)
	  })(window,document,'script','//www.google-analytics.com/analytics.js','ga');

	  ga('create', 'UA-55584370-8', 'auto');
	  ga('send', 'pageview');
	  
	  function purchase_validate() {
		if($("#agree_agreement").prop('checked')) {
			return true;
		}
		
		$("#error_validation").modal('show')
		return false;
	  }
	  
	  function selectProduct() {
		if($("#provider_type").val() == "TSCGQDC4YR2MQ") {
			$("#seat1").html("Entity Framework Extensions $799 (1 developer seat)");
			$("#seat2_4").html("Entity Framework Extensions $999 (2-4 developer seats)");
			$("#seat5_9").html("Entity Framework Extensions $1199 (5-9 developer seats)");
			$("#seat10_14").html("Entity Framework Extensions $1399 (10-14 developer seats)");
			$("#seat15_19").html("Entity Framework Extensions $1599 (15-19 developer seats)");
		}
		else {
			$("#seat1").html("Entity Framework Extensions $599 (1 developer seat)");
			$("#seat2_4").html("Entity Framework Extensions $799 (2-4 developer seats)");
			$("#seat5_9").html("Entity Framework Extensions $999 (5-9 developer seats)");
			$("#seat10_14").html("Entity Framework Extensions $1199 (10-14 developer seats)");
			$("#seat15_19").html("Entity Framework Extensions $1399 (15-19 developer seats)");
		}
	  }
	  
	  selectProduct();
	</script>
	<script>
/* smooth scrolling */
$(document).ready(function(){
	$('a[href*="#"]:not([href="#"])').click(function() {
		if (location.pathname.replace(/^\//,'') == this.pathname.replace(/^\//,'') 
			|| location.hostname == this.hostname) {

			var target = $(this.hash);
			target = target.length ? target : $('[name=' + this.hash.slice(1) +']');
			   if (target.length) {
				 $('html,body').animate({
					 scrollTop: target.offset().top
				}, 1000);
				return false;
			}
		}
	});
});
</script>
	</body>
</html>
