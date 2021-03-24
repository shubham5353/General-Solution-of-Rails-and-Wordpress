Chmod Reable File

sudo chmod -R 777 folder_name

python -m SimpleHTTPServer 8000

-------------------------------------------------------------------------------------------------------------------------------------


Rails Date

<li class="post-date"><strong><%= w.date.strftime("%d") %></strong><span><%= w.date.strftime("%b") %></span></li>
 if !b= nil? --check
-------------------------------------------------------------------------------------------------------------------------------------

WordPress Working With Date

$date = date_create($obj->field('blog_date'));
$blog_day = date_format($date,"d");
$blog_month = date_format($date,"M");
$blog_year = date_format($date,"y");

<?php echo $blog_day ?>/<?php echo $blog_month ?>/<?php echo $blog_year ?>

--------------------------------------------------------------------------------------------------------------------------------------

Rails current date and time

<%= Time.zone.now.strftime("%d/%m/%Y") %>

--------------------------------------------------------------------------------------------------------------------------------------

Latest Three blog in Wordpress

orderby="post_date DESC" limit="3"

--------------------------------------------------------------------------------------------------------------------------------------

Text Center Style

style=" display: flex; justify-content: center; align-items: center; flex-wrap: wrap; flex-direction: column;"

style="position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%);"

-------------------------------------------------------------------------------------------------------------------------------------

Modal Center

.vertical-alignment-helper {
    display:table;
    height: 100%;
    width: 100%;
}
.vertical-align-center {
    display: table-cell;
    vertical-align: middle;
}
.modal-content {
    width:inherit;
    height:inherit;
    margin: 0 auto;
}


------------------------------------------------------------------------------------------------------------------------------------

Black Overlay on image

box-shadow: inset 0 0 0 2000px rgba(0,0,0,.7);

Or

.overlay:before {
    position: absolute;
    content: '';
    width: 100%;
    height: 100%;
    top: 0;
    left: 0;
    background: #292929;
    opacity: .5;
    z-index: 2;
}

------------------------------------------------------------------------------------------------------------------------------------

BaguetteBox Lightbox

<link rel="stylesheet" type="text/css" href="https://cdnjs.cloudflare.com/ajax/libs/baguettebox.js/1.11.0/baguetteBox.css"> 
<script src="https://cdnjs.cloudflare.com/ajax/libs/baguettebox.js/1.11.0/baguetteBox.js"></script>
<script>
 baguetteBox.run('.gallery');
</script>

------------------------------------------------------------------------------------------------------------------------------------

Git

1- delete hide file in rail app that is .git
2- git status
3- git log
4- git init
5- git add .
6- git commit -m "Inital starting point from Shubham"
7- git remote add origin https://agile_software_partners@bitbucket.org/agile_software_partners/miraki_designs.git
8- git push -u origin master 

------------------------------------------------------------------------------------------------------------------------------------

Alternate blocking

 <% Event.all.each_with_index do |e, idx | %>
  <% if idx%2 == 0 %>
    <content1>
  <% else %>
    <content2>
<% end %>
<% end %>

------------------------------------------------------------------------------------------------------------------------------------

owl brand center just add class owl-centered to parent div

.owl-centered .owl-wrapper {
  display: table !important;
}
.owl-centered .owl-item {
  display: table-cell;
  float: none;
  vertical-align: middle;
}
.owl-centered .owl-item > div {
  text-align: center;
}

-------------------------------------------------------------------------------------------------------------------------------------

half half usp

1-   <% half_usp = @service.service_usps.count / 2 %> ---parent div
2-   <% @service.service_usps.limit(half_usp).offset(0).each do |s| %>   ---- first col
3-   <% @service.service_usps.limit(half_usp).offset(half_usp).each do |s| %>  ----second col

-------------------------------------------------------------------------------------------------------------------------------------

Scroll To Top 

  <button class="scroltop fa fa-chevron-up" style="display: inline-block;"></button>

	var scrollTop = function (){
		'use strict';
		var scrollTop = jQuery("button.scroltop");
		scrollTop.on('click',function() {
			jQuery("html, body").animate({
				scrollTop: 0
			}, 1000);
			return false;
		})

		jQuery(window).on("scroll", function() {
			var scroll = jQuery(window).scrollTop();
			if (scroll > 900) {
				jQuery("button.scroltop").fadeIn(1000);
			} else {
				jQuery("button.scroltop").fadeOut(1000);
			}
		});
		
		/* page scroll top on click function end*/
	}

-------------------------------------------------------------------------------------------------------------------------------------

WordPress Service Positioning

orderby="position_alphabetical ASC"

-------------------------------------------------------------------------------------------------------------------------------------

Wordpress Image Id

<?php 
$img = pods_image_url($obj->field('before_image'), 'Before After Image');
?>

<?php echo $img ?>

-------------------------------------------------------------------------------------------------------------------------------------

WordPress Permalink

<?php echo get_permalink($obj->field('id')); ?>

where service id-------

where='service.ID = {@ID}'

show on homepage-------

where="show_on_homepage.meta_value = 1"

-----Header & Footer link-------

<?php echo get_permalink(575) ?>

<?php 
$url_link = get_permalink($obj->field('client_section_button_link'));
?>
<?php echo $url_link ?>

--------------------------------------------------------------------------------------------------------------------------------------

Wordpress Incerase Number

<?php echo $obj->position(); ?>

--------------------------------------------------------------------------------------------------------------------------------------

Wordpress Alternating Block

<?php if ($obj->position() % 2 == 0) { ?>
<?php } else { ?>
<?php } ?>

--------------------------------------------------------------------------------------------------------------------------------------

JS Of Owl-Carousel

<script>
        $(document).ready(function(){
          $(".owl-carousel").owlCarousel({
            loop:true,
            margin:50,
            center:true,
            autoplay:true,
            responsiveClass:true,
            autoplaySpeed:1000,
            nav:true,
            dots: true,
            responsive:{
                0:{
                    items:1
                },
                600:{
                    items:3
                },
                1000:{
                    items:5
                }
            }
        })
     });
</script>


--------------------------------------------------------------------------------------------------------------------------------------

Center Logo in Carousel

<div class="item" style="height: 200px; position: relative;">
 <img src="<%= c.logo%>" style="position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%);">
</div>

--------------------------------------------------------------------------------------------------------------------------------------

Wordpress Things

so, if you need to link to "home" from the nav or footer, or logo etc, use the following:
 <?php echo get_home_url(); ?>

and if you need to link to a particular page, use the following: <?php echo esc_url( get_page_link( 258 ) ); ?>

id will get you in going to particular pages

style="background: url('<?php echo wp_get_attachment_url(5534); ?>'); this is what we use for image url, if we need to put in template

id will get in media

Service Nav -------------------

[pods template="Service Cat Nav Item" name="service_category" limit="-1" orderby="position_alphabetical ASC"]

Service Cat Nav Item for this we have to make template and in it...

[pods template="Service Nav Item" name="service" limit="-1" orderby="alphabetical ASC" where="service_category.ID = '{@ID}'"]

---------------------------------------------------------------------------------------------------------------------------------------


Filtering in Wordpress

<?php 
$filtering_class = sanitize_title($obj->field('portfolio_tab.post_title'));
?>

<div class="cbp-item all <?php echo $filtering_class ?>">

project name = E comm Developer
---------------------------------------------------------------------------------------------------------------------------------------

Wordpress Service ui li 


.home_service li:before {
    color: #ee2c24;
    content: "\f00c";
    font-family: FontAwesome;
    display: inline-block;
    margin-left: -1.9em;
    width: 2em;
}

---------------------------------------------------------------------------------------------------------------------------------------

Hide particular block or anything when not marked to particular service

<?php
    $porfolio_items = pods( 'service_portfolio', array(
      'where' => 'service.ID = ' . $obj->field('id')
    )); 
    $number_of_items = $porfolio_items->total();
    if ($number_of_items > 0) {
?>

........................................................................................................................................

Social Media color

.fa-linkedin {
  color: #0e76a8;
}

.fa-twitter {
  color: #00acee;
}

.fa-pinterest{
  color: #e13138;
}

.fa-youtube {
  color: #ef4e41;
}

.fa-instagram {
  color: #3f729b;
}

.fa-facebook {
  color: #3b5998;
}


------------------------------------------------------------------------------------------------------------------------------------------

Wordpress Half Half Service --example in Ecomm Developer

<?php 
$services = pods( 'service', array(
  'where' => 'show_on_footer.meta_value = 1'
)); 
$number_of_services = $services->total();
$half_number_of_services = $number_of_services / 2;
$remaning_services = $number_of_services - $half_number_of_services;
?>
                
<div class="col-lg-5 col-md-6 col-12">
    <div class="single-widget f-link widget">
        <h3 class="widget-title">Popular Services</h3>
        <div class="row">
            <div class="col-sm-6">
                <ul>
		         [pods name="service" template="Footer Popular Service Item"
			 where="show_on_footer.meta_value = 1" 
			 orderby="footer_position ASC"
			 limit="<?php echo $half_number_of_services ?>"
			 offset="0"]
                </ul>
            </div>
            <div class="col-sm-6">
                <ul>
		         [pods name="service" template="Footer Popular Service Item"
			 where="show_on_footer.meta_value = 1"
			 orderby="footer_position ASC" 
			 limit="<?php echo $remaning_services ?>"
			 offset="<?php echo $half_number_of_services ?>"]
                </ul>
            </div>
        </div>
    </div>
</div>


------- pods inside    <li><a href="<?php echo get_permalink($obj->field('id')); ?>">{@footer_name}</a></li>

----------------------------------------------------------------------------------------------------------------------------------

Active class Tab example in Mill Creek

<div class="panel panel-default">
    <div class="panel-heading" role="tab" id="h_faq<?php echo $obj->position(); ?>">
        <h4 class="panel-title">
            <a role="button" data-toggle="collapse" data-parent="#faq_acc" href="#c_faq<?php echo $obj->position(); ?>" aria-expanded="true" aria-controls="c_faq<?php echo $obj->position(); ?>">
                {@post_title}
                <i class="fa fa-caret-right" aria-hidden="true"></i>
            </a>
        </h4>
    </div>
    <div id="c_faq<?php echo $obj->position(); ?>" class="panel-collapse collapse <?php if ( $obj->position() == 1) echo 'in'; ?>" role="tabpanel" aria-labelledby="h_faq<?php echo $obj->position(); ?>">
        <div class="panel-body">
            {@description}
        </div>
    </div>
</div>

------------------------------------------------------------------------------------------------------------------------------------

Media Image Upload with Id

<?php echo wp_get_attachment_url(3427); ?>

-----------------------------------------------------------------------------------------------------------------------------------

View More Button Toggle example in https://www.millcreekpartners.com/

<style>
#about_us_learn_more_text {
display: none;
}

<section id="home_page_about_us">

<div id="about_us_learn_more_text">
{@about_us_more_description_text}
</div>
<div class="text-center">
	<button class="green_submit_btn" id="home_about_learn_more">View More</button>
</div>

</section>

<script>
document.addEventListener("DOMContentLoaded", function(){
	 $("#home_about_learn_more").click(
	 	function() {
	 		$("#about_us_learn_more_text").toggle('slow');
	 	}
	 );
});
</script>

-------------------------------------------------------------------------------------------------------------------------------------

Show and Hide content on mobile and desktop

.show_on_mobile {
  display: none;
}

.show_on_desktop {
  display: block;
}

@media (max-width: 768px) {
  .show_on_mobile {
    display: block;
  }

  .show_on_desktop {
    display: none;
  }
}


-----------------------------------------------------------------------------------------------------------------------------------------

javascript for null social media 

<script type="text/javascript">
document.addEventListener("DOMContentLoaded", function(){
    $(".socials a[href='']").css('display', 'none');
});
</script>

-----------------------------------------------------------------------------------------------------------------------------------------

Open A modal after 3 second on load 

<script>
document.addEventListener("DOMContentLoaded", function(){
  setTimeout(function(){

 $('#popup').modal('show');
}, 3000);
</script>

-----------------------------------------------------------------------------------------------------------------------------------------

Live Website Content Changing

<script type="text/javascript">
	
document.addEventListener('DOMContentLoaded', function () {
  var theSelector = "body.lf_page_home > div.main-wrapper > section:nth-child(3) > div > div > div > div > 
  div.section-heading.center > span";

document.querySelector(theSelector).innerHTML = "Introducing Louiz Innovations";

});

</script>
-------------------------------------------------------------------------------------------------------------------------------------------

Submit Button link to custom page in wordpress

<script type="text/javascript">
document.addEventListener("DOMContentLoaded", function(){
   
var wpcf7Elm = document.querySelector( '.wpcf7' );
 
wpcf7Elm.addEventListener( 'wpcf7mailsent', function( event ) {
  window.location.replace("https://gnedufair.com/thank-you-page/thank-you/");
}, false );

});
</script>


-------------------------------------------------------------------------------------------------------------------------------------------

String Trucate in Wordpress

<?php 
$description = wp_trim_words($obj->field('short_description'));
?>

<?php echo $description ?>
-------------------------------------------------------------------------------------------------------------------------------------------

For Blank hide full block in rails 

<% Spree::Client.limit(1).each do |c| %>
<% unless c.logo.blank?  %>

 ----content block----

<% end %>
<% end %>

-------------------------------------------------------------------------------------------------------------------------------------------
Wordpress Boolean Function

  <?php if ( $obj->field('hide_top_bar') != '1' ) { ?>
    ----content----
  <?php } ?>

-------------------------------------------------------------------------------------------------------------------------------------------

Deployment 

Here is a link to the video that explains the whole thing: https://youtu.be/2gZzxXkS5EQ

Credentials
BitBucket User Name: shubham_livefire
BitBucket Pushing Password: zQq2z2KxGuaPnvBQDqw2

Netifly Login:
shubham@livefire.in
shubhamf9#

Git Commands
git init .
git add .
git commit -m "Set Up Static"
git remote add origin https://shubham_livefire@bitbucket.org/shubham_livefire/[CHNAGE_ME].git
git push -uf origin master

--------------------------------------------------------------------------------------------------------------------------------------------

Website Language Change

1- add this div just below body tag ---  <div id="google_translate_element"></div>

2- Second add this script below

	<script type="text/javascript">

	function googleTranslateElementInit() {
	new google.translate.TranslateElement({pageLanguage: 'en', layout: google.translate.TranslateElement.InlineLayout.SIMPLE}, 'google_translate_element');
	}

	document.addEventListener("DOMContentLoaded", function(){
	$("body").prepend('<div id="google_translate_element"></div>');
	$.getScript("//translate.google.com/translate_a/element.js?cb=googleTranslateElementInit");
	});

	</script>


--------------------------------------------------------------------------------------------------------------------------------------------

Wordpress Social Share

<ul>
        <li>
            <a href="https://www.facebook.com/sharer/sharer.php?u=<?php
                     echo urlencode(get_permalink($obj->field('id')));
                     ?>" target="blank"> <i class="fa fa-facebook"></i> </a>
        </li>
        <li>
            <a href="http://twitter.com/share?url=<?php
                     echo urlencode(get_permalink($obj->field('id')));
                     ?>" target="blank"> <i class="fa fa-twitter"></i> </a>
        </li>
        <li>
            <a href="whatsapp://send?text=<?php echo urlencode(get_permalink($obj->field('id'))); ?>" target="blank"> <i class="fa fa-whatsapp"></i> </a>
        </li>
        <li>
            <a href="https://www.linkedin.com/shareArticle?mini=true&url=<?php echo urlencode(get_permalink($obj->field('id'))); ?>" target="blank"> <i class="fa fa-linkedin"></i> </a>
        </li>
</ul>


---------------------------------------------------------------------------------------------------------------------------------------------
