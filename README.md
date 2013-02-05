<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>HEALTH (Circle) </title>
    <meta name="description" content="">
    <meta name="author" content="">

    <!-- HTML5 shim, for IE6-8 support of HTML elements -->
    <!--[if lt IE 9]>
      <script src="http://html5shim.googlecode.com/svn/trunk/html5.js"></script>
    <![endif]-->

    <!-- styles -->
    <link type="text/css" href="/css/bootstrap-1.2.0.css" rel="stylesheet" />
    <link type="text/css" href="/css/circles.css" rel="stylesheet" />
    <link type="text/css" href="/css/smoothness/jquery-ui-1.8.17.custom.css" rel="stylesheet" />
    <link type="text/css" href="/js/plupload/js/jquery.ui.plupload/css/jquery.ui.plupload.css" rel="stylesheet" />

    <!-- javascript -->
    <script src="/js/jquery.js"></script>
    <script type="text/javascript" src="/js/jquery-ui.min.js"></script>

    <!-- fav and touch icons -->
    <link rel="shortcut icon" href="/images/favicon.ico">
    <link rel="apple-touch-icon" href="/images/apple-touch-icon.png">
    <link rel="apple-touch-icon" sizes="72x72" href="/images/apple-touch-icon-72x72.png">
    <link rel="apple-touch-icon" sizes="114x114" href="/images/apple-touch-icon-114x114.png">
    

  </head>

  <body>

    <!-- Topbar
    ================================================== -->
    <div class="topbar">
      <div class="topbar-inner">
        <!-- div class="container" -->
          
          <h3><a href="/stream">Policy Circles</a></h3>
          
          <ul class="nav">
              <li><a href="/profiles">Profiles</a></li>
              <li><a href="/events">Events</a></li>
              
              <li class="dropdown"><a href="#" class="dropdown-toggle">Circles</a>
  	<ul id="circle-menu" class="dropdown-menu">
		  <li><a href="/circle/edit/">New Circle...</a></li>
		  <li><a id="user_id" name="7b2540fcebd1e8b627aa6f52f70001a2"></a><a id="get-circles" href="/circles/">View Circles</a></li>
		  		  <!-- li>
		    <div class="input input-prepend menu-checkbox">
		      <label class="add-on">Your Private Circles <input id="view-private" type="checkbox" /></label>
		    </div>
		  </li>
		  <li>
		    <div class="input input-prepend menu-checkbox">
		      <label class="add-on">Your Public Circles <input id="view-public" type="checkbox" /></label>
		    </div>
		  </li>
		  <li>
		    <div class="input input-prepend menu-checkbox">
		      <label class="add-on">All Public Circles <input id="view-all" type="checkbox" /></label>
		    </div>
		  </li -->
		  		</ul>
	      </li>
          
          </ul>
          <ul class="nav secondary-nav">
              
              
                <li class="dropdown">
                <a href="#" class="dropdown-toggle">Trevor Banga</a>
                  <ul class="dropdown-menu">
                    <li><a href="/profile/edit/Trevor Banga">edit profile</a></li>
                    <li><a href="/switch_user">switch user</a></li>
                    <li><a href="/logout">Logout</a></li>
                </ul>
              
          </ul>
        <!-- /div -->
      </div>
    </div>

    <div class="container">
        <section id="notify">
        
        
        </section>

        <section id="content">
        
<script type="text/javascript" src="/js/nicEdit.js"></script>
<script type="text/javascript" src="/js/jquery.multiselect.min.js"></script>
<script type="text/javascript">
    
var circle_name = 'HEALTH';
var user_id     = '7b2540fcebd1e8b627aa6f52f70001a2';

var comment_holder;
var summary_holder;

$(document).ready(function(){

    $("#comment-form").validate({
	submitHandler: function() {
	    nicEditors.findEditor('comment-box').saveContent();
	    var comment_text = nicEditors.findEditor('comment-box').getContent();
	    console.log ("Comment: " + comment_text);
	    if (comment_text.length > 4){
		if (post_comment(comment_text)){
		    console.log("Looks good.");
		}
		else {
		    console.log("No good!");
		}
		nicEditors.findEditor('comment-box').setContent('');
	    }
	    return false;
	}
    });


  $('#document').validate({
    submitHandler: function(){
      nicEditors.findEditor('document-summary').saveContent();
      var document_summary = nicEditors.findEditor('document-summary').getContent();
      console.log ("Summary: " + document_summary);

	if (post_document(document_summary)){
	    console.log("Looks good.");
	}
	else {
	    console.log("No good!");
	}
	nicEditors.findEditor('comment-box').setContent('');

      return false;

    }
   });

$("#audience")
   .multiselect({
      noneSelectedText: 'Who should read this?',
      selectedList: 6
   });
    
});

$(function () {
    $('.tabs a:first').tab('show')
})

bkLib.onDomLoaded(function() {
    var icon_path = '/images/nicEditorIcons.gif';
    var button_list = [
	'bold',
	'italic',
	'underline',
	'strikeThrough',
	'ol',
	'ul',
	'image',
	'link',
	'unlink'];
 
    comment_holder = new nicEditor({
	iconsPath  : icon_path,
	buttonList : button_list,
	maxHeight  : 150
    }).panelInstance('comment-box');

    comment_holder.panelInstance('document-summary');

});

</script>
<script type="text/javascript" src="/js/bootstrap-tab.js"></script>
<script type="text/javascript" src="/js/circle-comment-stream.js"></script>

<div class="container">
    <div class="row">
        <div class="span12 column">
            <div id="HEALTH" class="circle-comments">
                <h1>Welcome to HEALTH</h1>
                <p><strong>What condition our condition is in</strong></p>
                
                <hr />
		<div class="comment-stream">
                  
                    <div class="well" id="f3608a09d98b1e3e9bec6f3a7f009739">
		    
                      <div>
			<span class="label success">DISCUSSION</span>
			
			<a name=""><span class="label notice">HEALTH</span></a>
		      </div>
                    <h1 itemprop="name headline  " style="margin-bottom: 2px; border-collapse: collapse; border-right-color: rgb(0, 97, 166); border-bottom-color: rgb(0, 97, 166); border-left-color: rgb(0, 97, 166); font-family: georgia, serif; font-weight: normal; font-size: 2.166em; line-height: 1.154; width: 460px; color: rgb(51, 51, 51); text-align: start; background-repeat: no-repeat no-repeat;">International development: big questions, small answers</h1><p itemprop="description" id="stand-first" class="stand-first-alone" data-component="comp : r2 : Article : standfirst_cta" style="padding-bottom: 34px; margin-bottom: 0px; border-collapse: collapse; font-family: arial, sans-serif; color: rgb(102, 102, 102); font-size: 1.333em; line-height: 1.25; width: 460px; background-repeat: no-repeat no-repeat;">In place of the searching global conversation we need, we have an anaesthetised debate</p>
                    <br />
		    
		    <small>
		      
                      <a href="/profile/Trevor Banga">
                        Trail posted by Trevor Banga</a> -
		      
                      <a class="prettyDate" title="2013-01-21T15:40:11Z">2013-01-21T15:40:11Z</a>
                    </small>
                  </div>
                  
                    <div class="well" id="f3608a09d98b1e3e9bec6f3a7f008777">
		    
                      <div>
			<span class="label success">DISCUSSION</span>
			<a name=""><span class="label notice">HEALTH</span></a>
		      </div>
                    <p style="margin-bottom: 13px; border-collapse: collapse; font-family: arial, sans-serif; color: rgb(51, 51, 51); font-size: 14px; background-repeat: no-repeat no-repeat;">Something is lacking in the efforts to design a new&nbsp;<a href="http://www.guardian.co.uk/global-development" title="More from guardian.co.uk on Global development" style="border-collapse: collapse; color: rgb(0, 86, 137); background-repeat: no-repeat no-repeat;">global development</a>framework. The aim – to set&nbsp;<a href="http://www.guardian.co.uk/commentisfree/2011/dec/30/global-development-reimagining-the-goals" title="" style="border-collapse: collapse; color: rgb(0, 86, 137); background-repeat: no-repeat no-repeat;">goals for all mankind and the planet</a>&nbsp;– ought to involve all the great questions of the age. Instead, the discussion feels small and technocratic. Despite great efforts, it has attracted derisory attention from beyond the professional development world.</p><p style="margin-bottom: 13px; border-collapse: collapse; font-family: arial, sans-serif; color: rgb(51, 51, 51); font-size: 14px; background-repeat: no-repeat no-repeat;">The high-level panel is becoming an overused, or at least a misused, instrument. The&nbsp;<a href="http://www.un.org/sg/management/hlppost2015.shtml" title="" style="border-collapse: collapse; color: rgb(0, 86, 137); background-repeat: no-repeat no-repeat;">latest on this theme</a>, chaired by David Cameron together with the presidents of Indonesia and Liberia, has been given too many members and too little time. NGOs, when asked how to replace&nbsp;<a href="http://www.un.org/millenniumgoals/" title="" style="border-collapse: collapse; color: rgb(0, 86, 137); background-repeat: no-repeat no-repeat;">the millennium development goals</a>, simply listed all the issues that&nbsp;<a href="http://www.ustream.tv/recorded/26635441" title="" style="border-collapse: collapse; color: rgb(0, 86, 137); background-repeat: no-repeat no-repeat;">kept them in business</a>. Then there are the online forums for public engagement. Under the alluring question "what kind of world do you want?", the discussion is immediately splintered into scores of&nbsp;<a href="http://www.worldwewant2015.org/sitemap" title="" style="border-collapse: collapse; color: rgb(0, 86, 137); background-repeat: no-repeat no-repeat;">technical questions and papers</a>. Another site simply offers a vote between such apples and oranges as "better job opportunities" or "an honest and responsive government". In place of the searching global conversation we need, we have an anaesthetised debate.</p><p style="margin-bottom: 13px; border-collapse: collapse; font-family: arial, sans-serif; color: rgb(51, 51, 51); font-size: 14px; background-repeat: no-repeat no-repeat;">Peculiarly unable to criticise itself, the development community is proving unable to lead a debate about changing the world. Profound work has been done with aid, like slashing child mortality in Africa, and without aid, such as the UN Development Programme's reporting on the Arab world. But reduced poverty rates owe more to Deng Xiaoping than any development agency. Skewed incentives, a&nbsp;<a href="http://www.nybooks.com/articles/archives/2010/nov/25/foreign-aid-scoundrels/?pagination=false" title="" style="border-collapse: collapse; color: rgb(0, 86, 137); background-repeat: no-repeat no-repeat;">patchy human rights record</a>, chaotic structures, hubristic prescriptions and one-size-fits-all solutions all blight development, and so too does a penchant for technical solutions to political problems. The debate needs blasting open. Most poverty is now found in powerful states, and most extreme poverty now found amid war. Thus human rights, peace and security all need placing centre stage. So too do those inclusive international institutions which provide one of the few real protections the weak have against the strong. All of this is, after all, the agenda of&nbsp;<a href="http://www.un.org/millennium/declaration/ares552e.htm" title="" style="border-collapse: collapse; color: rgb(0, 86, 137); background-repeat: no-repeat no-repeat;">the millennium declaration</a>, which the MDGs purported to serve.</p><p style="margin-bottom: 13px; border-collapse: collapse; font-family: arial, sans-serif; color: rgb(51, 51, 51); font-size: 14px; background-repeat: no-repeat no-repeat;">While the questions in development are getting bigger, the professional and intellectual scene has never been so fragmented. It will take a formidable alchemy to forge strong solutions here. One thing is clear: wasting years on a technocratic debate about goals which are for advocacy more than anything else – and likely drawn up without reference to such fundamentals as political rights – is not a serious response to the dysfunctional summitry, procrastination and missed targets of recent years. And it will leave the global public square in the same state of disrepair. The conversation we need has barely begun.</p>
                    <br />
		    
		    <small>
		      
                      <a href="/profile/Dan McGarry">
                        Trail posted by Trevor Banga</a> -
		      
                      <a class="prettyDate" title="2013-01-21T14:35:30Z">2013-01-21T14:35:30Z</a>
                    </small>
                  </div>
                  
                    <div class="well" id="f3608a09d98b1e3e9bec6f3a7f00738e">
		    
                      <div>
			<span class="label success">DISCUSSION</span>
			<a name=""><span class="label notice">HEALTH</span></a>
		      </div>
                    <h1 style="margin-bottom: 20px; font-size: 24px; font: inherit; vertical-align: baseline; outline: 0px; background-color: transparent; color: rgb(0, 89, 140); font-family: Times; text-align: left;"><a href="http://andrewsullivan.thedailybeast.com/2013/01/the-limits-of-political-morality-.html" style="cursor: pointer; color: rgb(0, 89, 140); font-size: 24px; vertical-align: baseline; background-color: transparent;">The Moral Genius Club</a></h1><p style="margin-bottom: 20px; font-size: 15px; font: inherit; vertical-align: baseline; outline: 0px; background-color: transparent; line-height: 1.4em; color: rgb(0, 0, 0); font-family: Times;">Charles Fried&nbsp;<a href="http://www.tnr.com/article/books-and-arts/magazine/111233/humanity-in-war" target="_self" style="cursor: pointer; color: rgb(0, 89, 140); font-size: 15px; vertical-align: baseline; background-color: transparent;">reads</a>&nbsp;John Fabian Witt’s&nbsp;<a href="http://www.amazon.com/Lincolns-Code-Laws-American-History/dp/1416569839/ref=sr_1_1?ie=UTF8&amp;qid=1358284235&amp;sr=8-1&amp;keywords=lincoln%27s+code" target="_self" style="cursor: pointer; color: rgb(0, 89, 140); font-size: 15px; vertical-align: baseline; background-color: transparent;"><em style="font-size: 15px; font: inherit; vertical-align: baseline; outline: 0px; background-color: transparent;">Lincoln’s Code</em></a>&nbsp;as "an extended tribute to Lincoln’s moral genius":</p><blockquote style="margin-right: 20px; margin-bottom: 20px; margin-left: 20px; padding-top: 20px; padding-right: 10px; padding-left: 10px; border-top-width: 1px; border-bottom-width: 1px; border-top-style: dotted; border-bottom-style: dotted; border-top-color: rgb(193, 193, 193); border-bottom-color: rgb(193, 193, 193); font-size: 15px; font: inherit; vertical-align: baseline; quotes: none; outline: 0px; background-color: rgb(241, 241, 241); line-height: 1.4em; color: rgb(0, 0, 0); font-family: Times;"><p style="margin-bottom: 20px; font-size: 15px; font: inherit; vertical-align: baseline; outline: 0px; background-color: transparent; line-height: 1.4em;">Moral genius, like political genius, is far closer to artistic genius than it is to genius in science or mathematics. It has to do with putting together familiar elements in unexpected ways, combining and recombining the materials to take account of and overcome the constraints of those materials, and finally coming up with a whole that surprises by its power, its aptness, and its sense that we are experiencing something fundamentally new. Relating moral genius to the genius of Keats or Raphael or Bach may seem to diminish the ultimate seriousness, the urgency of morality — or at least to make a category mistake that slights the special quality of each. But they do have things in common. In each case we cannot look at the world again in the same way after we have taken them in. Everything that has gone before and comes after takes on a different valence and hue.</p></blockquote><p style="margin-bottom: 20px; font-size: 15px; font: inherit; vertical-align: baseline; outline: 0px; background-color: transparent; line-height: 1.4em; color: rgb(0, 0, 0); font-family: Times;">Alan Jacobs&nbsp;<a href="http://www.theamericanconservative.com/jacobs/on-moral-genius/" target="_self" style="cursor: pointer; color: rgb(0, 89, 140); font-size: 15px; vertical-align: baseline; background-color: transparent;">wonders</a>&nbsp;who counts as a moral genius:</p><blockquote style="margin-right: 20px; margin-bottom: 20px; margin-left: 20px; padding-top: 20px; padding-right: 10px; padding-left: 10px; border-top-width: 1px; border-bottom-width: 1px; border-top-style: dotted; border-bottom-style: dotted; border-top-color: rgb(193, 193, 193); border-bottom-color: rgb(193, 193, 193); font-size: 15px; font: inherit; vertical-align: baseline; quotes: none; outline: 0px; background-color: rgb(241, 241, 241); line-height: 1.4em; color: rgb(0, 0, 0); font-family: Times;"><p style="margin-bottom: 20px; font-size: 15px; font: inherit; vertical-align: baseline; outline: 0px; background-color: transparent; line-height: 1.4em;">For a Christian such as myself, Jesus is the obviously ideal exemplar of moral genius, but the category would obviously apply to other founders of religious traditions: the Buddha, Moses, Mohammed, etc. Below this obvious highest level, I wonder whom else we might identify as moral geniuses? The prophet Isaiah, certainly; St. Francis of Assisi; Maimonides; in a peculiar but important sense Montaigne.</p><p style="margin-bottom: 20px; font-size: 15px; font: inherit; vertical-align: baseline; outline: 0px; background-color: transparent; line-height: 1.4em;">Anyone care to nominate others?</p></blockquote>
                    <br />
		    
		    <small>
		      
                      <a href="/profile/Dan McGarry">
                        Trial posted by Trevor Banga</a> -
		      
                      <a class="prettyDate" title="2013-01-21T14:16:36Z">2013-01-21T14:16:36Z</a>
                    </small>
                  </div>
                  
                    <div class="well" id="653fc482c4a0729182775f42a7010791">
		    
                      <div>
			<span class="label success">DISCUSSION</span>
			<a name=""><span class="label notice">HEALTH</span></a>
		      </div>
                    Coolio!
                    <br />
		    
		    <small>
		      
                      <a href="/profile/Dan McGarry">
                        Trial posted by Trevor Banga</a> -
		      
                      <a class="prettyDate" title="2013-01-17T17:19:58Z">2013-01-17T17:19:58Z</a>
                    </small>
                  </div>
                  
                    <div class="well" id="653fc482c4a0729182775f42a700eb87">
		    
                      <div>
			<span class="label success">DISCUSSION</span>
			<a name=""><span class="label notice">HEALTH</span></a>
		      </div>
                    <h1 style="margin-bottom: 20px; font-size: 24px; font: inherit; vertical-align: baseline; outline: 0px; background-color: transparent; color: rgb(0, 89, 140); font-family: Times; text-align: left;"><a href="http://andrewsullivan.thedailybeast.com/2013/01/did-assad-use-chemical-weapons.html" style="cursor: pointer; color: rgb(0, 89, 140); font-size: 24px; vertical-align: baseline; background-color: transparent;">Did Assad Use Chemical Weapons?</a></h1><p style="margin-bottom: 20px; font-size: 15px; font: inherit; vertical-align: baseline; outline: 0px; background-color: transparent; line-height: 1.4em; color: rgb(0, 0, 0); font-family: Times;">A video&nbsp;<a href="http://www.buzzfeed.com/rosiegray/horrifying-videos-of-possible-chemical-weapons-vic" target="_self" style="cursor: pointer; color: rgb(0, 89, 140); font-size: 15px; vertical-align: baseline; background-color: transparent;">claiming</a>&nbsp;to show a chemical weapons victim:</p><p style="margin-bottom: 20px; font-size: 15px; font: inherit; vertical-align: baseline; outline: 0px; background-color: transparent; line-height: 1.4em; color: rgb(0, 0, 0); font-family: Times;"><iframe frameborder="0" height="315" src="http://www.youtube.com/embed/uLc4zoAmbRE" width="560" style="margin: 0px; padding: 0px; border-width: 0px; font-size: 15px; font: inherit; vertical-align: baseline; outline: 0px; background-color: transparent;"></iframe></p><p style="margin-bottom: 20px; font-size: 15px; font: inherit; vertical-align: baseline; outline: 0px; background-color: transparent; line-height: 1.4em; color: rgb(0, 0, 0); font-family: Times;">Raffi Khatchadourian<a href="http://www.newyorker.com/online/blogs/newsdesk/2013/01/the-case-of-agent-15-did-syria-use-a-nerve-agent.html" target="_self" style="cursor: pointer; color: rgb(0, 89, 140); font-size: 15px; vertical-align: baseline; background-color: transparent;">&nbsp;pieces together</a>&nbsp;conflicting information on the attack:</p><blockquote style="margin-right: 20px; margin-bottom: 20px; margin-left: 20px; padding-top: 20px; padding-right: 10px; padding-left: 10px; border-top-width: 1px; border-bottom-width: 1px; border-top-style: dotted; border-bottom-style: dotted; border-top-color: rgb(193, 193, 193); border-bottom-color: rgb(193, 193, 193); font-size: 15px; font: inherit; vertical-align: baseline; quotes: none; outline: 0px; background-color: rgb(241, 241, 241); line-height: 1.4em; color: rgb(0, 0, 0); font-family: Times;"><p style="margin-bottom: 20px; font-size: 15px; font: inherit; vertical-align: baseline; outline: 0px; background-color: transparent; line-height: 1.4em;">[W]as the gas used in Homs akin to sarin? No and yes, it seems. Sarin is odorless, and people in Homs reported smelling the chemical. Sarin is hyper-potent, and some people apparently inhaled a lot of this gas without dying. If these details are correct, then the compound surely differs from sarin in significant ways. And yet, there are similar chemicals out there that cause the same symptoms but are not nearly as potent and do have an odor. They are orgaonphosphate pesticides, which happen to be among the most common pesticides in the world and are also cholinesterase inhibitors. They can cause symptoms identical to their military counterparts, including death, and are treatable with atropine. If the chemical used in Homs was a commercial pesticide, then it appears that someone has manufactured a crude, poor-man’s chemical weapon out of a commonly available item.</p></blockquote>
                    <br />
		    
		    <small>
		      
                      <a href="/profile/Dan McGarry">
                        Trial posted by Trevor Banga</a> -
		      
                      <a class="prettyDate" title="2013-01-17T16:35:55Z">2013-01-17T16:35:55Z</a>
                    </small>
                  </div>
                  
		</div>
                <hr />
            </div>
        </div>
        <div class="span3 column offset1">
            <p class="right">
	    
            
  	      
	    
            
            
	      
            <a id="self-subscribe-button" href="#" name="/circle/subscribe?circle=HEALTH&username=Trevor Banga" class="btn primary">subscribe</a>
            
            
            </p>
            
            
            
        </div>
    </div>
</div>

<script type="text/javascript">
var options, a;

jQuery(function(){
        options = { lookup:["Crumblestiltskin","Dan McGarry","Lenz","Trevor Banga"] };
        a = $('#autoComplete').autocomplete(options);
        });
</script>

        </section>
    </div>


    <div id="footer">
      <div class="inner">
        <div class="container">
          <p class="right"><a href="#">Back to top</a></p>
          <p>
            Designed and built by <a href="http://policycircles.com" target="_blank">Policy Circles</a><br />
          </p>
        </div>
      </div>
    </div>

    <!-- Javascript includes go here -->
    <script src="/js/jquery.autocomplete-min.js"></script>
    <script src="/js/jquery.markdown-0.2.js"></script>
    <script src="/js/jquery.prettydate.js"></script>
    <script src="/js/jquery.validate.min.js"></script>
    <script src="/js/bootstrap-alerts.js"></script>
    <script src="/js/circles.js"></script>
    <script src="/js/application.js"></script>
  </body>
</html>
