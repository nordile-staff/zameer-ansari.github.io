---
layout: post
title: C# code documentation
---

![Documentation please](http://www.webpal.net/blog/wp-content/uploads/2011/11/clutter_cartoon_3.png)

[courtesy](http://www.webpal.net/blog/tag/document-management-2/)

The golden rule of code documentation:

> Try to document [why](http://stackoverflow.com/a/4929769) (code design decisions) and avoid what (code design descriptions).

To keep up with the increasing complexity of the project, it's very important to document the coding decisions. It's one of the best practices.

[Visual studio](https://www.visualstudio.com/) provides some elegant ways for code documentation to keep the code understandable. It can also understand the changes that one make on hard code.

# Single or multi line comments

 - Short (or long) functional descriptions

<pre>
<code class="csharp">
	//single line comment
</code>
</pre>

These are necessary to describe functionality in little.

<pre>
  <code class="csharp">
	
	/*
	multiple
	line
	comments
	*/
	
</code>
</pre>

Avoid them. It is advisable to avoid writing essays about code. The end product shall be code not their long descriptions.

# Collapsible regions

 - Summary of the functional block

<pre>
  <code class="csharp">
	
	#region Some code block

	//some code here
    	//some foo bar
    	//Fizz Buzz
    	//some unicorns
    
	#endregion
    
</code>
</pre>


Regions are collapsible. Just hover over the collapsed region and get a glance.

![Glance in collapsed code](http://i.imgur.com/wsEL9yo.png)

[courtesy](http://imgur.com/)

# Summary

 - Summary of the function or property

<pre>
<code class="csharp">
	
	/// &lt;summary&gt;
        /// Summary description for the function or property goes here
        /// &lt;/summary&gt;
        
     </code>
</pre>

![summary method description](http://i.imgur.com/ksUWv5O.png)

[courtesy](http://imgur.com/)

 - Summary of the function parameter

<pre>
<code class="csharp">
        /// &lt;param name="TestParameter"&gt;Summary description for the parameter goes here&lt;/param&gt;
     </code>
</pre>

![parameter desc](http://i.imgur.com/zwKtSLt.png)

[courtesy](http://imgur.com/)

Visual studio changes this section after change of the parameter name.

![Change of parameters](http://i.imgur.com/5RWuBMJ.png)

[courtesy](http://imgur.com/)

 - Summary of the returning stuff

<pre>
<code class="csharp">
	///&lt;returns&gt;Summary description for the function result goes here&lt;/returns&gt;
   </code>
</pre>

A simple example:

<pre>
<code class="csharp">

    /// &lt;summary&gt;
    /// Main class of the project
    /// &lt;/summary&gt;
    class Program
    {
        /// &lt;summary&gt;
        /// Main entry point of the program
        /// &lt;/summary&gt;
        /// &lt;param name="args"&gt;Command line args&lt;/param&gt;
        static void Main(string[] args)
        {
            //Do stuff
        }
    }
    
</code>
</pre>
