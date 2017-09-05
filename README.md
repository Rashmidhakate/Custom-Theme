# Custom-Theme
﻿
STEPS TO INSTALL CUSTOM THEME

Admin->CONTENT->DESIGN->Configuration->Apply custom theme

Required CMS Block to set up theme:

Content->Blocks->Add new Block

Header section:

1.)header left nev		
	 Identifier: header_left
	 Content:
<div class="supportandfollow cf">
	<span class="call-for-support">
		Call for support: 
		<a class="callto" href="tel:1800123456">1800 - 123 - 456</a>
	</span> 
	<span class="follow-us">
		Follow us : 
		<a href="#"><i class="fa fa-twitter"></i></a>
		<a href="#"><i class="fa fa-facebook"></i></a>
		<a href="#"><i class="fa fa-youtube-play"></i></a> 
		<a href="#"><i class="fa fa-google"></i></a> 
	</span>
</div>

2.)header right nev
	Identifier : header_right
	Content :
<div class="toplinks-baar">
<ul class="toplinks cf">
<li><a title="Register" href="{{store url="customer/account/create/"}}">Register</a></li>
<li><a title="Login" href="{{store url="customer/account/login/"}}">Login</a></li>
<li><a title="Account" href="{{store url="customer/account/"}}">Account</a></li>
<li><a title="Wishlist" href="{{store url="wishlist"}}">Wishlist</a></li>
<li class="searchblok">{{block class="Magento\Framework\View\Element\Template" name="top.search" as="topSearch" template="Magento_Search::form.mini.phtml"}}</li>
</ul>
</div>


Home Page Content Area:

3.)Banner Block
	Identifier : banner
	Content:
		<p><img src="{{view url="images/banner.jpg"}}" alt="" width="100%" height="621" /></p>
	
4.)Best Seller Product Block
	Identifier : best_seller_product
	Content:
<div class="container">
<h2><span>Best Sellers</span></h2>
<div class="cf">
<div class="lasting-beauty"><img src="{{view url="images/lasting-beauty.jpg"}}" alt="Lasting Beauty" />
<div class="lasting-beauty-title"><span>New Collection 17/18</span>Lasting Beauty</div>
</div>
<div class="bestsaller-product">{{block class="Magehit\Bestsellerproducts\Block\Home\BestsellerList" name="bestseller_data" template="bestsellerblock.phtml"}}</div>
</div>
</div>

5.)Feature Product Block/Sale Product(Here I have added feature product and use widget for It)
	Identifier : feature_product_block
	Content:
<div class="container">
<h2><span>Sale Products</span></h2>
<div class="cf">
<div class="lasting-beauty"><img src="{{view url="images/sale-products.jpg"}}" alt="Sale Products" /></div>
<div class="bestsaller-product">{{widget type="Magento\CatalogWidget\Block\Product\ProductsList" show_pager="0" products_count="10" template="product/widget/content/grid.phtml" conditions_encoded="a:2:[i:1;a:4:[s:4:`type`;s:50:`Magento|CatalogWidget|Model|Rule|Condition|Combine`;s:10:`aggregator`;s:3:`all`;s:5:`value`;s:1:`1`;s:9:`new_child`;s:0:``;]s:4:`1--1`;a:4:[s:4:`type`;s:50:`Magento|CatalogWidget|Model|Rule|Condition|Product`;s:9:`attribute`;s:11:`is_featured`;s:8:`operator`;s:2:`==`;s:5:`value`;s:1:`1`;]]"}}</div>
</div>
</div>

6.) New Product Block(I have added widget for new product)
	Identifier : new_product_block
	Content: 
<div class="container">
<h2><span>New Arrivals</span></h2>
{{widget type="Magento\\Catalog\\Block\\Product\\Widget\\NewWidget" template="product/widget/new/content/new_grid.phtml"}}
<div class="cf">
<div class="bestsaller-product">
<div class="cf">
<div class="offerimg offerimgleft"><span><img src="{{view url="images/off-on-powder-mackup.jpg"}}" alt="" /></span></div>
<div class="offerimg offerimgright"><span><img src="{{view url="images/sale-bloger.jpg"}}" alt="" /></span></div>
</div>
<ul class="makeup cf">
<li>
<div class="imgmain"><img src="{{view url="images/makeup.jpg"}}" alt="" /></div>
<div class="makeup-detail">
<h3>makeup</h3>
<ul class="description cf">
<li><a title="Makeup Palettes " href="#">Makeup Palettes </a></li>
<li><a title="Makeup remover" href="#">Makeup remover</a></li>
<li><a title="Nails &amp; Lips" href="#">Nails &amp; Lips</a></li>
</ul>
<a class="view-all" title="View all" href="#">View all <i class="fa fa-caret-right"></i> </a></div>
</li>
<li>
<div class="imgmain"><img src="{{view url="images/skin-care.jpg"}}" alt="" /></div>
<div class="makeup-detail">
<h3>skin care</h3>
<ul class="description cf">
<li><a title="Face &amp; Eyes" href="#">Face &amp; Eyes</a></li>
<li><a title="Lip Care" href="#">Lip Care</a></li>
<li><a title="Bath &amp; Body" href="#">Bath &amp; Body</a></li>
</ul>
<a class="view-all" title="View all" href="#">View all <i class="fa fa-caret-right"></i> </a></div>
</li>
<li>
<div class="imgmain"><img src="{{view url="images/hair-care.jpg"}}" alt="" /></div>
<div class="makeup-detail">
<h3>hair care</h3>
<ul class="description cf">
<li><a title="Shampoo" href="#">Shampoo</a></li>
<li><a title="Conditioner" href="#">Conditioner</a></li>
<li><a title="Styling Products" href="#">Styling Products</a></li>
</ul>
<a class="view-all" title="View all" href="#">View all <i class="fa fa-caret-right"></i> </a></div>
</li>
<li>
<div class="imgmain"><img src="{{view url="images/fragrance.jpg"}}" alt="" /></div>
<div class="makeup-detail">
<h3>fragrance</h3>
<ul class="description cf">
<li><a title="Makeup Palettes " href="#">Makeup Palettes </a></li>
<li><a title="Makeup remover" href="#">Makeup remover</a></li>
<li><a title="Nails &amp; Lips" href="#">Nails &amp; Lips</a></li>
</ul>
<a class="view-all" title="View all" href="#">View all <i class="fa fa-caret-right"></i> </a></div>
</li>
<li>
<div class="imgmain"><img src="{{view url="images/luxury-beauty.jpg"}}" alt="" /></div>
<div class="makeup-detail">
<h3>Luxury beauty</h3>
<ul class="description cf">
<li><a title="Face &amp; Eyes" href="#">Face &amp; Eyes</a></li>
<li><a title="Lip Care" href="#">Lip Care</a></li>
<li><a title="Bath &amp; Body" href="#">Bath &amp; Body</a></li>
</ul>
<a class="view-all" title="View all" href="#">View all <i class="fa fa-caret-right"></i> </a></div>
</li>
<li>
<div class="imgmain"><img src="{{view url="images/men-grooming.jpg"}}" alt="" /></div>
<div class="makeup-detail">
<h3>Men&rsquo;s Grooming</h3>
<ul class="description cf">
<li><a title="Shampoo" href="#">Shampoo</a></li>
<li><a title="Conditioner" href="#">Conditioner</a></li>
<li><a title="Styling Products" href="#">Styling Products</a></li>
</ul>
<a class="view-all" title="View all" href="#">View all <i class="fa fa-caret-right"></i> </a></div>
</li>
</ul>
<div class="productbig-review cf">
<div class="productbig-img">
<div class="productbig-img-main"><img src="{{view url="images/should-body-care-products-be-scented.jpg"}}" alt="" />
<div class="product-detail"><span class="title">Should body care products be scented? We discussed.....</span>
<ul class="userandtime">
<li><i class="fa fa-user-o"></i> Jane Doe</li>
<li><i class="fa fa-clock-o"></i> 15m ago</li>
</ul>
</div>
</div>
</div>
<div class="productbig-img">
<div class="productbig-img-main"><img src="{{view url="images/perfact-nails-and-brows.jpg"}}" alt="" />
<div class="product-detail"><span class="title">Perfact Nails And Brows</span>
<ul class="userandtime">
<li><i class="fa fa-user-o"></i> Jane Doe</li>
<li><i class="fa fa-clock-o"></i> 15m ago</li>
</ul>
</div>
</div>
</div>
<div class="productbig-img">
<div class="productbig-img-main"><img src="{{view url="images/elizabeth-arden.jpg"}}" alt="" />
<div class="product-detail"><span class="title">Elizabeth Arden Flawless Finish Sponge On Cream Makeup</span>
<ul class="userandtime">
<li><i class="fa fa-user-o"></i> Jane Doe</li>
<li><i class="fa fa-clock-o"></i> 15m ago</li>
</ul>
</div>
</div>
</div>
</div>
</div>
</div>
</div>

7.)Brand Logo
	Identifier : brand_logo
	Content: 
<div class="container brandlogos-row">
<ul class="brandlogos cf">
<li><a title="" href="#"><img src="{{view url="images/brand-logo1.jpg"}}" alt="" /></a></li>
<li><a title="" href="#"><img src="{{view url="images/brand-logo2.jpg"}}" alt="" /></a></li>
<li><a title="" href="#"><img src="{{view url="images/brand-logo3.jpg"}}" alt="" /></a></li>
<li><a title="" href="#"><img src="{{view url="images/brand-logo4.jpg"}}" alt="" /></a></li>
<li><a title="" href="#"><img src="{{view url="images/brand-logo5.jpg"}}" alt="" /></a></li>
</ul>
<div class="footerlink-address cf">
<div class="footer-colun">
<h3>contact us</h3>
<span class="contact-no">1900 - 123 - 456</span> <span class="openingday">Monday - Friday: 8.00 AM - 9.00 PM</span> <span class="openingday">Saturday: 9.00 AM - 9.00 PM</span> <span class="openingday">Sunday: 9.00 AM - 9.00 PM</span></div>
<div class="footer-colun">
<h3>Store List</h3>
<address>
<h4>Warehouse &amp; Offices</h4>
<span>12345 Street name,<br />California, USA<br />0123 456 789 / 0123 456 788</span>
<h4>Retail Shop</h4>
<span>12345 Street name,<br />California, USA<br />0123 456 789 / 0123 456 788</span></address></div>
<div class="footer-colun">
<h3>Account</h3>
<ul class="footerlinks">
<li><a title="Wishlist" href="{{store url="wishlist"}}">Wishlist</a></li>
<li><a title="Your Account" href="#">Your Account</a></li>
<li><a title="Checkout" href="#">Checkout</a></li>
<li><a title="Login" href="{{store url="customer/account/login/"}}">Login</a></li>
</ul>
</div>
<div class="footer-colun">
<h3>information</h3>
<ul class="footerlinks">
<li><a title="About Us" href="{{store url="about-us"}}">About Us</a></li>
<li><a title="Jobs" href="#">Jobs</a></li>
<li><a title="Affiliates" href="#">Affiliates</a></li>
<li><a title="Contact US" href="{{store url="contact"}}">Contact US</a></li>
</ul>
</div>
<div class="footer-colun">
<h3>Categories</h3>
<ul class="footerlinks">
<li><a title="Makeup" href="#">Makeup</a></li>
<li><a title="Skin Care" href="#">Skin Care</a></li>
<li><a title="Hair Care" href="#">Hair Care</a></li>
<li><a title="Fragrance" href="#">Fragrance</a></li>
<li><a title="Luxury Beauty" href="#">Luxury Beauty</a></li>
<li><a title="Men&rsquo;s Grooming" href="#">Men&rsquo;s Grooming</a></li>
</ul>
</div>
</div>
</div>


Footer Section

8.)Footer Block
	Identifier : footer_block	
	Content:
<footer>
<div class="container">
<ul class="footermenu">
<li>&copy; 2017</li>
<li><a title="Privacy" href="{{store url="about-us"}}">Privacy</a></li>
<li><a title="Terms" href="#">Terms</a></li>
<li><a title="Sitemap" href="#">Sitemap</a></li>
</ul>
<ul class="cards">
<li><a title="American Express" href="#"><img src="{{view url="images/american-express-card.jpg"}}" alt="American Express" /></a></li>
<li><a title="Discover" href="#"><img src="{{view url="images/discover-card.jpg"}}" alt="Discover" /></a></li>
<li><a title="MasterCard" href="#"><img src="{{view url="images/master-card.jpg"}}" alt="MasterCard" /></a></li>
<li><a title="PayPal" href="#"><img src="{{view url="images/paypal-card.jpg"}}" alt="PayPal" /></a></li>
<li><a title="Visa" href="#"><img src="{{view url="images/visa-card.jpg"}}" alt="Visa" /></a></li>
<li><a title="Skrill" href="#"><img src="{{view url="images/skrill-card.jpg"}}" alt="Skrill" /></a></li>
</ul>
<a class="move-top" title="top" href="#">Top</a></div>
</footer> 



Call CMS block on home Page

Content->Pages->HomePage

Homepage Content:

<div class="banner">{{block class="Magento\\Cms\\Block\\Block" block_id="banner"}}</div>
<div class="full-row border-bottom top-bottom-space">{{block class="Magento\\Cms\\Block\\Block" block_id="best_seller_product"}}</div>
<div class="full-row border-bottom top-bottom-space sale-products">{{block class="Magento\\Cms\\Block\\Block" block_id="feature_product_block"}}</div>
<div class="full-row border-bottom top-bottom-space sale-products new-arrivals-main">{{block class="Magento\\Cms\\Block\\Block" block_id="new_product_block"}}</div>
