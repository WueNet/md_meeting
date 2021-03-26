# Markdown Cheat-Sheet

<a style="background-color:yellow;color:black">This file was created in typora, it won't look as good in GitHub Markdown.</a>   



## 1. What is Markdown?

- Markdown is a simple lay-out syntax that can easily  be rendered or transposed into HTML. You can think of it as easy-peasy-mini-HTML but without doing actual markup stuff (i.e., using tags as in HTML or XML (or TeX))
	- Recognized by a lot of Webbrowsers / websites
	- Used in the computational communities, e.g., Stack-Overflow or GitHub
	- Most markdown editors or webpages except HTML as well, when rendering a markdown file. 
- Why you should use (and to some extend embrace Markdown):
	- It is implemented in a lot of editors and webpages and gets more popular by the day.
	- Because its simplicity, it will soon enough be translatable to all your favorite text layout programs
		- Already compatible with HTML and TeX/LaTeX 
	- It is super lightweight, simple and open source: You can write plain markdown "source code" in any text editor and it will still be pretty readable.
	- There are some promising integrations of markdown which will help you organizing your workflows (e.g., Notebooks, Rmarkdown)
	- You can build your own markdown wiki.





## 2. Markdown Syntax

### 2.1. Layout Options in Markdown

- As described above, Markdown makes it easy to highlight sections and Text with just a couple of syntax characters.
- To escape any character, use backslash. E.g., \\\* escapes the Asterisk.



#### 2.1.1. Headings and Highlighting

##### 2.1.1.1. Headings and Paragraphs

- There are 6 Levels of Markdown headings, they are initiated with a number  of ``#``s:
	- ``# Highest Heading``
	- ``## Second Highest Heading``
	- `### Third Highest Heading`
	- `#### Fourth Highest Heading`
	- `##### Fifth Highest Heading`
	- `###### Sixth Highest / Lowest Heading`



- An empty line creates a new paragraph, Typora does it automatically, when you hit ENTER.

**Example**

This is my first paragraph and I separate it by hitting Enter

This is my second paragraph (See source code mode to check out the invisible line in-between).



- Two Spaces at the End of a line create  a line break without a new paragraph.
	- This might be relevant for some formatting, e.g. if you use the html `<br>` tag to force an empty line, this might lead to unwanted effects (a simple line break instead of an empty line in this case) if you don't use double space in the line before.

**Example**

- I separate my bullet points with (doesn't work in Github) `<br>`.<br>  
	- This only worked because of the double space after the ``<br>`` tag.



##### 2.1.1.2. Highlighting

- **Italics**: ``*stars for italics*`` = *stars for italics* (can also use underscores)
- **Strong**: `**double stars for bold**` = **double stars for bold**
- **Combinations**: `***triple stars*** or _underscores_ **for _combinations_**` = ***triple stars*** or _underscores_ **for _combinations_**
- **Strikethrough**: `~~tilde for strikethrough~~` = ~~tilde for strike through~~ 
- **HTML_color**: ``<a style="color:purple">doesn't work on github</a>`` = <a style="color:purple">doesn't work on github</a>

- **Horizontal rule**: ``___``just use three underscores:

	___





##### 2.1.1.3. Code Highlighting

- For inline code use simple \` around the text, that you want to write as code.
- For code boxes use three \` and the programming language you want to highlight.

```markdown
​```markdown
This is would create a Markdown-Codebox.
​```

This: `here` would create inline code.
```





#### 2.1.2. Lists

- **Unordered Lists**: You initiate an unordered list with any of the following signs: ``-``, `+`, `*`
	- But since minus (`-`) is popular in other editors as well and asterisk is also used for italics, I recommend sticking with ``-``.
	- You can add a deeper level with tab or two spaces.
- **Ordered Lists**: 
	- You can use any kind of 1., a., etc. instead of the above examples to create an ordered list. The most useful feature here is, that you don't have to specify the numeration, you could just always write `1.` For all list elements in all levels and markdown will render it perfectly into numbered lists.  You can also combine ordered and unordered lists (check out source code):

1. one
1. two
	1. Another level
		* third level with unordered bullet points
		* third level with unordered bullet points



- **Check-Lists** (GitHub Flavored MD): In Github you can create checkboxes with this syntax:

	```
	- [ ] an empty checkbox
	- [x] a checked checkbox
	```
- [ ] empty checkbox
- [x] a checked checkbox 







#### 2.1.3. Quotation

- Use ``>`` or iterations of ``>`` for regular and nested versions of the markdown quote highlighting

	- ``> Quote``= 

		> Quote

	- Combine the above with an additional ``> Nested quote`` for nested quotes:

		> Quote
		>
		> > Nested quote





#### 2.1.4. Links

##### 2.1.4.1. URLs and Between Document Links

Syntax: **``[visible link](Address)``**

- Use a URL, or a file path to link websites or files (e.g., other markdown files)
	- ``visible link``: what ever you want to see in the rendered text
	- ``Address``: wherever your link points to:
		- A URL: e.g., ``[google](https://www.google.com)``
		- A path: e.g., ``~/Documents/important_md_file.md``
			- Tipp: use relative paths! ``..`` for "one folder up from file location" is allowed (e.g., ``../sister_folder/sister-daughter_folder/file``! 
- You can also use HTML (see below)





##### 2.1.4.2. Within Document Links

- You can link to a section in a markdown file (sometimes called jump mark) by two ways:

	1. Use the link syntax and a ``#`` + a section header to create a Link towards that section.

		``[visible link](#1. What is Markdown?)``

	2. Like 1. But instead of jumping to a section you can also jump to a named HTML tag. 

		``<a name="jump here"> visible text to jump to </a>``  + the actual link: ``[visible link](#jump here)``





### 2.1.5. HTML in Markdown

- There are differences in what HTML is rendered by e.g., GitHub Markdown vs. Typora's Markdown.
	- For example, Github doesn't accept the color-options in a style parameter like ``<a style="color:pink">colored text</a>``.
- Generally speaking, a lot of simple HTML coding is correctly rendered by most markdown programs.
- Here I represent three example of HTML in a Markdown-file which I found quite helpfull.
	- Tip: use ``<div>`` to trigger a HTML-block in Typora



##### 2.1.5.1. Images

- I like to use the image tag to place and scale my images in a markdown file.

	- e.g., the following code produces the below output:

		```html
		<div>
			<img src="cropped-leibnizdream-logo3-2.png" style="margin-left:10%;margin-right:60%;width:30%">
		  		<figcaption style="margin-left:15%;margin-right:65%"><i>Figure:</i> LeibnizDream Logo looks nice</figcaption>
			</img>
		</div>
		```

<div>
		<img src="cropped-leibnizdream-logo3-2.png" style="margin-left:10%;margin-right:60%;width:30%">
  		<figcaption style="margin-left:15%;margin-right:65%"><i>Figure:</i> LeibnizDream Logo looks nice</figcaption>
	</img>
</div>



##### 2.1.5.2. Preserve

- Another useful tag is ``<pre>`` if you want to keep the output. You can combine it with the font-tag to have, e.g., a mono-space font.

	- Attention: not all fonts are supported in all Markdown Programms / Editors.

	- e.g., the following code produces the below output:

		```html
		<pre><font face="Courier New">
		This			will			keep				all 			
					my				white			space
							as					typed
										!
		</font></pre>
		```

		<pre><font face="Courier New">
		This			will			keep				all 			
					my				white			space
							as					typed
										!
		</font></pre>

		


##### 2.1.5.3. links etc.





### 2.1.6. Math Mode

$$
‎\cos x‎ ‎=‎ ‎‎\sum_{n=0}^{\infty} ‎\frac{(ix)^{2n‎}}{(2n)!}‎‎
$$


$$
\ new\ math\ block
$$

$$
\mathrm{[[the]_D\ man_N]_{NP}}
$$







## 2.2. Useful Keyboard Shortcuts

