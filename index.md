---
layout: blog
title: Blog
image: "../assets/page_images/blog.jpg"
slogan1: So you are here...
slogan2: Get started !!!!
---


<div class="main">
		<ul class="blog-list">
		{% for post in site.posts %}
			<li>
				<figure class="" >
						{% if post.image %}
						
							<a href="{{ post.url }}" title="" style="background-image: url({{ post.image }})"></a>
						
						{% else %}
						
							<a href="{{ post.url }}" title="" style="background-image: url({{ site.baseurl }}assets/post_images/{{post.post_for}}.png)"></a>												
							
						{% endif %}
				
				</figure>
				<div class="blog-content">            
					<h3><a href="{{ post.url }}">{{ post.title }}</a></h3>            
						<ul>
							<li>
							<time>
								<span class="posted-on">
									<time>
										<time class="entry-date published">{{ post.date | date_to_string }}</time>
									</time>
								</span>
							</time>
							</li>
						</ul>
					<p>{{ post.content | strip_html | truncatewords:30 }}</p>
				</div>
			</li>
		{% endfor %}	
		</ul>
</div>