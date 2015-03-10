# Schema.org Documentation Summary
Schema.org provides a collection of shared vocabularies webmasters can use to mark up their pages in ways that can be understood by the major search engines: Google, Microsoft, Yandex and Yahoo!

You use the schema.org vocabulary along with the [Microdata](http://en.wikipedia.org/wiki/Microdata_(HTML)), [RDFa](http://en.wikipedia.org/wiki/RDFa), or [JSON-LD](http://en.wikipedia.org/wiki/JSON-LD) formats to add information to your Web content.

- [Official Documentation Schema.org](http://schema.org)

## Why use microdata?
Web pages have an underlying meaning that people understand when they read the web pages. But search engines have a limited understanding of what is being discussed on those pages. By adding additional tags to the HTML of your web pages—tags that say, "Hey search engine, this information describes this specific movie, or place, or person, or video"—you can help search engines and other applications better understand your content and display it in a useful, relevant way. Microdata is a set of tags, introduced with HTML5, that allows you to do this.

##How to mark up your content using microdata (Steps)
1.  **itemscope and itemtype**

	1.  identify the section of the page that is about the item. To do this, add 	the `itemscope` element to the HTML tag that encloses information about the 	item
		
			<div itemscope>
				...
			</div>
	
	2. By adding `itemscope`, you are specifying that the HTML contained in the 	`<div>...</div>` block is about a particular item.
	
	3. But it's not all that helpful to specify that there is an item being 	discussed without specifying what kind of an item it is. You can specify the 	type of item using the `itemtype` attribute immediately after the `itemscope`. 	Say Example is an Movie

			<div itemscope itemtype="http://schema.org/Movie">
				...
			</div>
		
	4. This specifies that the item contained in the `div` is in fact a Movie, as 	defined in the schema.org type hierarchy. **Item types** are provided as URLs, 	in this case `http://schema.org/Movie`.

2.	**itemprop** 
	
	1. To label properties of an item, use the `itemprop` attribute. For example, 	to identify the director of a movie, add `itemprop="director"` to the element 	enclosing the director's name.
	
			<div itemscope itemtype ="http://schema.org/Movie">
  				<h1 itemprop="name">Title Film</h1>
  				<span>
  					Director: <span itemprop="director">Direcors Name</span> (born August 16, 1954)
  				</span>
  			
  				<span itemprop="genre">Genre of Movie</span>
  				<a href="../link-to-trailer.html"itemprop="trailer">Trailer</a>
			</div>
3. **Embedded Items**
	
