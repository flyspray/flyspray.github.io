---
layout: default
title: "Flyspray: The bug killer!"
---


<div class="jumbotron">
	<p>
		Flyspray is an uncomplicated, web-based bug tracking system written in PHP for assisting with software development. Originally developed for the <a href="http://www.psi-im.org/">Psi Jabber client</a> project it has been made available to everyone under the GPL 2.1 licence.
	</p>
	<div class="btn-group btn-group-justified ">
		<a class="btn btn-success btn-lg" href="{{ site.baseurl }}/docs/download">Download</a>
		<a class="btn btn-info btn-lg" href="{{ site.baseurl }}/community/mailing-list">Mailing List</a>
		<a class="btn btn-primary btn-lg" href="{{ site.baseurl }}/manual">Manual</a>
	</div>
</div>

<div class="row">
	<div class="col-md-7">
		<h3>News<h3>
			{% for news in site.categories["news"] limit:4 %}
				<h4><a href="{{ site.baseurl }}{{ news.url }}">{{ news.title }}</a></h4>
				{{ news.summary }}
				<hr>
	        {% endfor %}
	</div>
	<div class="col-md-5">
		<div class="well well-lg">
			<h3>Features Include:</h3>

			<ul>
				<li>Web-based, platform-independent</li>
				<li>Multiple database support, currently MySQL and PGSQL</li>
				<li>Easy installation</li>
				<li>Easy to use</li>
				<li>Multiple projects</li>
				<li>'Watching' tasks, with notification of changes (email or <a href="http://jabber.rocks.cc/" rel="noreferrer">Jabber</a>)</li>
				<li>Comprehensive task history</li>
				<li>File attachments</li>
				<li>CSS themes</li>
				<li>Advanced search features (though easy to use)</li>
				<li>Atom/RSS feeds</li>
				<li>Two syntax options for task descriptions and more (Dokuwiki / plain text)</li>
				<li>Voting for tasks</li>
				<li>Dependency graphs</li>
				<li>Activity Bars for projects and user activity</li>
				<li>Comments</li>
				<li>Roadmaps</li>
			</ul>
		</div>
	</div>
</div>

<h3>Screenshots</h3>
<div class="row">
  <div class="col-xs-8 col-md-4">
    <a href="images/screenshots/screenshot1.png" class="thumbnail">
		<img alt="" src="images/screenshots/screenshot1-thumb.png">
	</a>
  </div>
  <div class="col-xs-8 col-md-4">
    <a href="images/screenshots/screenshot2.png" class="thumbnail">
		<img alt="" src="images/screenshots/screenshot2-thumb.png">
	</a>
  </div>
  <div class="col-xs-8 col-md-4">
    <a href="images/screenshots/screenshot2.png" class="thumbnail">
		<img alt="" src="images/screenshots/screenshot3-thumb.png">
	</a>
  </div>
</div>
<div class="row">
  <div class="col-xs-8 col-md-4">
    <a href="images/screenshots/screenshot4.png" class="thumbnail">
		<img alt="" src="images/screenshots/screenshot4-thumb.png">
	</a>
  </div>
  <div class="col-xs-8 col-md-4">
    <a href="images/screenshots/screenshot5.png" class="thumbnail">
		<img alt="" src="images/screenshots/screenshot5-thumb.png">
	</a>
  </div>
  <div class="col-xs-8 col-md-4">
    <a href="images/screenshots/screenshot6.png" class="thumbnail">
		<img alt="" src="images/screenshots/screenshot6-thumb.png">
	</a>
  </div>
</div>
