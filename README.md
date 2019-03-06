<html>
	<head>
		<meta charset="UTF-8" />
		<title>ｙｏ　ｓｋｒｉｌｌ</title>
		<!--<link rel="icon" href="img/favi.png" sizes="16x16 32x32 48x48 150x150" type="image/vnd.microsoft.icon" />-->
		<link rel="icon" href="img/favicon.png" sizes="16x16 32x32 48x48 150x150" type="image/vnd.microsoft.icon" />
		<script type="text/javascript" src="jquery-1.11.3.min.js"></script>
		<script type="text/javascript" src="https://www.google.com/jsapi"></script>
		<link rel="stylesheet" type="text/css" href="styles.css"/>
		<script type="text/javascript">
			
			$(document).ready(function(){
				  //URL of the RSS feed
				  $(".marquee").toggleClass("microsoft");
				  var feed_url = 'https://www.reddit.com/.rss';
				$.ajax({
				  url      : 'http://ajax.googleapis.com/ajax/services/feed/load?v=1.0&num=10&callback=?&q=' + encodeURIComponent(feed_url),
				  dataType : 'json',
				  success  : function (data) {
					if (data.responseData.feed && data.responseData.feed.entries) {
					  $.each(data.responseData.feed.entries, function (i, e) {
						$("#news1").append('<a target="_blank" class="mlink" href="' + e.link + '">' + e.title + '.</a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;');
					  });
					}
				  }
				});
			});
			
			function show( show1 ) {
			  document.getElementById(show1).style.display="block";
			}
			function hide( hide1 ) {
			  document.getElementById(hide1).style.display="none";
			}
			function tog( tog1 ) {
			  document.getElementById(tog1).style.backgroundColor="rgba(255,255,255,.8)";
			}
			function toh( toh1 ) {
			  document.getElementById(toh1).style.backgroundColor="rgba(255,255,255,.8)";
			}
		</script>
	</head>
	<body>
		<script type="text/javascript">
		var currentTime = new Date().getHours();
		if (currentTime <= 12) {
		    if (document.body) {
		        document.body.background = "img/1.jpg";
		    }
		}
		else {
		    if (document.body) {
		        document.body.background = "img/2.jpg";
		    }   
		}
		</script>
		<div class="maincontainer">
			<div class="bottomcontainer">
				<div class="button" id="btn1" onclick = "show('main1');hide('main2');tog('btn1');toh('btn2');"></div>
				<div class="button" id="btn2" onclick = "show('main2');hide('main1');tog('btn2');toh('btn1');"></div>

				<!--<div class="marqueebar" id="marqueebar">
					<marquee id="news1" class="marquee2"></marquee>
				</div> -->
				<div id="searchbar">
					<form name="form1" action="https://www.duckduckgo.com/?q=" method="get" >
						<input type="text" autocomplete="off" placeholder="ddg search..." name="q" class="searchinput"></input>
					</form>
				</div>
			</div>
			<div class="time" id="time">
				<script>
					//document.getElementById("main").innerHTML = Date();
					function updateClock() {
						var days = ['SUNDAY','MONDAY','TUESDAY','WEDNESDAY','THURSDAY','FRIDAY','SATURDAY'];
						var m = new Date();
						var dateString =
						  (days[ m.getDay() ]) + " " +
						  ("0" + (m.getMonth()+1)).slice(-2) +"/"+
						  ("0" + m.getDate()).slice(-2) + "/" +
						  m.getFullYear() +" "+
						  ("0" + m.getHours()).slice(-2) + ":" +
						  ("0" + m.getMinutes()).slice(-2) + ":" +
						  ("0" + m.getSeconds()).slice(-2);
						
						// set the content of the element with the ID time to the formatted string
						document.getElementById('time').innerHTML = dateString;
						// call this function again in 1000ms
						setTimeout(updateClock, 1000);
					}
					updateClock(); // initial call
				</script>
			</div>
			<div class="main" id="main1">
				<div class="sidebar" style="background-image: url(https://i.imgur.com/sFlvWnq.gif);"></div>
				<div class="welcome">いま すぐ ころして</div>
				<div class="bookmarkscontainer">
					<ul>
						<li><a href="http://mail.google.com/mail/u/1/">mail</a>/<a href="http://drive.google.com/drive/u/1/my-drive">drive</a>
						<li> <a href="https://sites.google.com/a/bisvietnam.net/bulletin/daily-bulletin">bulletin</a>
						<li><a href="https://classroom.google.com/u/1/h">class</a>/<a href="https://calendar.google.com/calendar/b/1/r?pli=1&t=AKUaPmZZ-x7QgrUY8jVxVwKIc8n7DRyZo5VgUt_N-4RoZOJYM0S2fGvibDt6e5ZHt-huisFQfCO7Ai7W-7iTkKVz0sEpZCpzEg%3D%3D">cal</a>
						<li><a href="https://khanacademy.org">khan</a>/<a href="http://www.color-hex.com/color-wheel/">wheel</a>
						<li><a href="https://github.com/Ax8000TauN">git</a>/<a href="https://bandcamp.com/tauneutrino/feed">bcamp</a>
						<li><a href="https://www.messenger.com">msg</a>/<a href="https://quizlet.com/latest">qlet</a>
					</ul>
					<ul>
						<li><a href="https://mail.google.com">mail</a>/<a href="https://outlook.live.com/mail/">outlk</a>
						<li><a href="https://dropbox.com">dropbox</a>
						<li><a href="https://www.youtube.com">ytube</a>/<a href="https://www.youtube.com/feed/subscriptions?flow=1">feed</a>
						<li><a href="http://tumblr.com/dashboard">dash</a>/<a href="https://innerspaceboy.tumblr.com">blog</a>
						<li><a href="https://www.deviantart.com/notifications/">watch</a>/<a href="https://www.pinterest.com/">pin</a>
						<li><a href="https://letterboxd.com/">ltboxd</a>
					</ul>
					<ul>
						<li><a href="https://reddit.com">front</a>/<a href="https://www.reddit.com/user/livinginfutility/saved/">saved</a>
						<li><a href="https://www.reddit.com/r/desktops/">r/desks</a>
						<li><a href="https://www.reddit.com/r/unixporn/">r/unixprn</a>
						<li> <a href="https://www.reddit.com/r/androidthemes/">r/android</a>
						<li><a href="https://www.reddit.com/r/terraria/">r/terraria</a>
						<li><a href="https://boards.4chan.org/wg/catalog">/wg/</a>
					</ul>
					<ul>
						<li><a href="http://thepiratebay.org">tpbay</a>
						<li><a href="https://idope.se/">idop</a>/<a href="https://torrents.me">tor.m</a>
						<li><a href="https://zooqle.com/">zqle</a>/<a href="https://www.reddit.com/r/megalinks/">r/mg</a>
						<li><a href="https://weboas.is/">weboasis</a>
						<li><a href="https://www.digbt.org/">digbt</a>
						<li><a href="https://rutracker.org/">rutrk</a>/<a href="http://en.metal-tracker.com/">mtal</a>
					</ul>
				</div>
			</div>
			<div class="main" id="main2" style="display:none">
				<div class="sidebar" style="background-image: url(img/12.gif);"></div>
				<div class="spotify"><iframe src="https://open.spotify.com/embed/user/12155397458/playlist/3AiuK3jgYtEOG0GeAo1dWl?si=oxBMhz6WQICGpitzNslMuQ" width="100%" height="100%" frameborder="0" allowtransparency="true" allow="encrypted-media"></iframe></div>		
			</div>
		</div>
	</body>
</html>
