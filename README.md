AgeGate
==========

About this Plugin:
==========

The AgeGate plugin is a JW Player Plugin that presents users with a prompt asking them to enter their birthday. If the users are older than the required age, they may watch the video. Otherwise, they are taken to a different page and are unable to view the video with under-aged viewers. Share AgeGate with your friends and prevent under-aged viewers from watching NSFW content.

###[Demo](http://www.pluginsbyethan.com/github/agegate.html)

Configuration Options:
==========

This plugin supports additional configuration options via flashvars.

agegate.minage: Minimum age of the viewer - Default is 18<br />
agegate.maxage: Maximum age of the viewer - Default is 100. Note: Do not set the date to before 1900.<br />
agegate.message: The message displayed if you do not meet the age criteria. - Default is You do not meet the age criteria for this video.<br />
agegate.redirecturl: The link provided if you do not meet the age criteria. Note: You will have to click the message to be redirected.<br />
agegate.redirecttarget: The target to open redirecturl in - Default is _blank<br />
agegate.backgroundcolor: Color of the curtain that covers the player - Default is #000000<br />
agegate.textcolor: Color of the text displayed on screen - Default is #FFFFFF<br />
agegate.subheadertextcolor: Color of the subheader text - Default is #FFCC00<br />
agegate.messagetextcolor: Color of the message text - Default is #FF0000<br />
agegate.cookielife: How long to set the cookie for. Default is 60 minutes.<br />
agegate.header: Header Text - Default is - The content in this video requires age verification.<br />
agegate.subheader: Subheader Text - Default is - Please enter your date of birth below:<br />
agegate.autoredirect: If you want to automatically redirect the user to the redirecturl if they do not meet the age criteria. The default is false, but set to true, if you want to enable this feature.<br />

Implementing this Plugin:
==========

There is one file that you need to use, agegate.js. Upload this file to your server, it can go anywhere on the server. Now, inside of your JW Player embed code, make sure that your plugins call points to the full path to the .js file on your server (http://www.yoursite.com/agegate.js).

Example:
==========

<pre>
&lt;script type=&quot;text/javascript&quot; src=&quot;jwplayer.js&quot;&gt;&lt;/script&gt;
&lt;div id=&quot;player&quot;&gt;&lt;/div&gt;
&lt;script type=&quot;text/javascript&quot;&gt;
jwplayer('player').setup({
&nbsp;&nbsp;'width': '575',
&nbsp;&nbsp;'height': '400',
&nbsp;&nbsp;'file': 'video.mp4'
&nbsp;&nbsp;'image': &quot;video.jpg&quot;,
&nbsp;&nbsp;plugins: {
	&nbsp;&nbsp;&nbsp;&nbsp;&quot;agegate.js&quot;: {
	&nbsp;&nbsp;}
&nbsp;&nbsp;}
});
&lt;/script&gt;
</pre>

The source code is available for this plugin. There is just a .js file for JavaScript. Publishing the JavaScipt can be simply done with any text editor. Enjoy~! :)
